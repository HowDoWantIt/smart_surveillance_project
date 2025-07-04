
Start
↓
Initialize Camera (VideoCapture)
↓
Load Modules

Motion Detection

Object Detection

Face Recognition

License Plate Recognition

Database

Logger
↓
Enter Infinite Loop (until stopped)
↓
Capture frame from camera
↓
Is frame captured?

No → End program

Yes → Continue
    ↓
Detect motion in frame
↓
Is motion detected?

No → Display frame without further processing

Yes → Continue
    ↓
Detect objects (people, animals, vehicles, etc.)
↓
For each detected object:
    If object is person:
        - Detect faces in frame
        - For each face:
            • Is face recognized?
                - Yes → Display name on image
                - No →
                    • Save unknown face image
                    • Store info in database
                    • Log alert
    If object is vehicle (car, motorcycle, truck, etc.):
        - Crop license plate image
        - Read plate text with OCR
        - Is plate valid?
            • Yes →
                - Save plate image
                - Store plate info in database
                - Log plate event
↓
Display frame with bounding boxes and info
↓
Is ESC key pressed?

Yes → End program

No → Loop back to capture next frame
↓
End

# Start with a minimal Go image
FROM golang:1.23

# Set the working directory in the container
WORKDIR /app

# Copy dependency files
COPY backend/go.mod backend/go.sum ./

# Download dependencies
RUN go mod download

# Copy the application code
COPY backend/ .

# Build the Go application
RUN go build -o main .

# Expose the application port
EXPOSE 8080

# Command to run the application
CMD ["./main"]

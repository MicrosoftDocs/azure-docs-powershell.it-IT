---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: CE1C6576-234E-4891-9158-FA45B64B786C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41e8641b01dcb95a6b6939ff3551fe03b642ddf0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023393"
---
# <span data-ttu-id="a9406-101">Set-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="a9406-101">Set-AzureStorSimpleVirtualDevice</span></span>

## <span data-ttu-id="a9406-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a9406-102">SYNOPSIS</span></span>
<span data-ttu-id="a9406-103">Crea o aggiorna la configurazione del dispositivo di un dispositivo virtuale StorSimple.</span><span class="sxs-lookup"><span data-stu-id="a9406-103">Creates or updates the device configuration of a StorSimple virtual device.</span></span>

## <span data-ttu-id="a9406-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a9406-104">SYNTAX</span></span>

```
Set-AzureStorSimpleVirtualDevice -DeviceName <String> -SecretKey <String> -AdministratorPassword <String>
 -SnapshotManagerPassword <String> [-TimeZone <TimeZoneInfo>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a9406-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9406-105">DESCRIPTION</span></span>
<span data-ttu-id="a9406-106">Il cmdlet **set-AzureStorSimpleVirtualDevice** crea o aggiorna la configurazione del dispositivo di un dispositivo virtuale di Azure StorSimple.</span><span class="sxs-lookup"><span data-stu-id="a9406-106">The **Set-AzureStorSimpleVirtualDevice** cmdlet creates or updates the device configuration of an Azure StorSimple virtual device.</span></span>

## <span data-ttu-id="a9406-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a9406-107">EXAMPLES</span></span>

### <span data-ttu-id="a9406-108">Esempio 1: aggiornare un dispositivo virtuale</span><span class="sxs-lookup"><span data-stu-id="a9406-108">Example 1: Update a virtual device</span></span>
```
PS C:\>$TimeZoneInfo = [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }
PS C:\> Set-AzureStorSimpleVirtualDevice -DeviceName "Contoso23" -SecretKey "wcZBlBGpCMf4USdSKyt/SQ==" -TimeZone $TimeZoneInfo
VERBOSE: ClientRequestId: e31f0d6b-451d-4c1d-b2f1-3fc84c13972c_PS
VERBOSE: ClientRequestId: df58db83-d563-4a2e-bbb4-9576f0e69ca6_PS
VERBOSE: ClientRequestId: 494a9f0d-79ee-4fde-ab4d-85ee5a357556_PS
VERBOSE: ClientRequestId: ce557cbf-174d-4301-93d4-5ffe082c8413_PS
VERBOSE: ClientRequestId: 31284dad-de2c-4758-a2ef-45962875bfa6_PS
VERBOSE: About to configure the device : win-ff93i74m1e1 ! 
VERBOSE: ClientRequestId: d9c66302-45d8-488a-adda-8ccf957f77d3_PS


TaskId       : 21f530c3-bc47-4591-8c4e-da4d694b751d
TaskResult   : Succeeded
TaskStatus   : Completed
ErrorCode    : 
ErrorMessage : 
TaskSteps    : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: a94f972c-18ea-40b6-9401-2ad209c0c8b4_PS
AlertNotification              : Microsoft.WindowsAzure.Management.StorSimple.Models.AlertNotificationSettings
Chap                           : Microsoft.WindowsAzure.Management.StorSimple.Models.ChapSettings
DeviceProperties               : Microsoft.WindowsAzure.Management.StorSimple.Models.DeviceInfo
DnsServer                      : Microsoft.WindowsAzure.Management.StorSimple.Models.DnsServerSettings
InstanceId                     : d369ebb4-8b9a-47fc-9a6b-60f371e123ae
Name                           : 
NetInterfaceList               : {}
OperationInProgress            : None
RemoteMgmtSettingsInfo         : Microsoft.WindowsAzure.Management.StorSimple.Models.RemoteManagementSettings
RemoteMinishellSecretInfo      : Microsoft.WindowsAzure.Management.StorSimple.Models.RemoteMinishellSettings
SecretEncryptionCertThumbprint : 
Snapshot                       : Microsoft.WindowsAzure.Management.StorSimple.Models.SnapshotSettings
TimeServer                     : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeSettings
Type                           : VirtualAppliance
VirtualApplianceProperties     : Microsoft.WindowsAzure.Management.StorSimple.Models.VirtualApplianceInfo
WebProxy                       : Microsoft.WindowsAzure.Management.StorSimple.Models.WebProxySettings

VERBOSE: Successfully updated configuration for device Contoso23 with id d369ebb4-8b9a-47fc-9a6b-60f371e123ae
```

<span data-ttu-id="a9406-109">Il primo comando usa la classe **System. TimeZoneInfo** .NET e la sintassi standard per ottenere il fuso orario Pacifico standard e archivia tale oggetto nella variabile $TimeZoneInfo.</span><span class="sxs-lookup"><span data-stu-id="a9406-109">The first command uses the **System.TimeZoneInfo** .NET class and standard syntax to get Pacific Standard Time zone, and stores that object in the $TimeZoneInfo variable.</span></span>

<span data-ttu-id="a9406-110">Il secondo comando Aggiorna il dispositivo denominato Contoso23 per usare il fuso orario specificato in $TimeZoneInfo.</span><span class="sxs-lookup"><span data-stu-id="a9406-110">The second command updates the device named Contoso23 to use the time zone specified in $TimeZoneInfo.</span></span>
<span data-ttu-id="a9406-111">Il comando richiede la chiave segreta per accedere alla configurazione del dispositivo virtuale.</span><span class="sxs-lookup"><span data-stu-id="a9406-111">The command requires the secret key to access the virtual device configuration.</span></span>

### <span data-ttu-id="a9406-112">Esempio 2: aggiornare un dispositivo virtuale usando l'operatore pipeline</span><span class="sxs-lookup"><span data-stu-id="a9406-112">Example 2: Update a virtual device by using the pipeline operator</span></span>
```
PS C:\> [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" } | Set-AzureStorSimpleVirtualDevice -DeviceName "Contoso23" -SecretKey "wcZBlBGpCMf4USdSKyt/SQ=="
```

<span data-ttu-id="a9406-113">Questo comando Aggiorna il dispositivo denominato Contoso23 per usare il fuso orario creato dal comando.</span><span class="sxs-lookup"><span data-stu-id="a9406-113">This command updates the device named Contoso23 to use the time zone that the command creates.</span></span>
<span data-ttu-id="a9406-114">Il comando richiede la chiave segreta per accedere alla configurazione del dispositivo virtuale.</span><span class="sxs-lookup"><span data-stu-id="a9406-114">The command requires the secret key to access the virtual device configuration.</span></span>
<span data-ttu-id="a9406-115">Questo comando funziona allo stesso modo dell'esempio precedente, ad eccezione del fatto che passa il fuso orario al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="a9406-115">This command works the same way as the previous example, except that it passes the time zone to the current cmdlet by using the pipeline operator.</span></span>

## <span data-ttu-id="a9406-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a9406-116">PARAMETERS</span></span>

### <span data-ttu-id="a9406-117">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="a9406-117">-AdministratorPassword</span></span>
<span data-ttu-id="a9406-118">Specifica la password di amministratore del dispositivo virtuale da configurare.</span><span class="sxs-lookup"><span data-stu-id="a9406-118">Specifies the administrator password of the virtual device to configure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9406-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a9406-119">-DeviceName</span></span>
<span data-ttu-id="a9406-120">Specifica il nome del dispositivo virtuale da configurare.</span><span class="sxs-lookup"><span data-stu-id="a9406-120">Specifies the name of the virtual device to configure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9406-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="a9406-121">-Profile</span></span>
<span data-ttu-id="a9406-122">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="a9406-122">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9406-123">-SecretKey</span><span class="sxs-lookup"><span data-stu-id="a9406-123">-SecretKey</span></span>
<span data-ttu-id="a9406-124">Specifica una chiave di crittografia del servizio per il dispositivo virtuale.</span><span class="sxs-lookup"><span data-stu-id="a9406-124">Specifies a service encryption key for the virtual device.</span></span>
<span data-ttu-id="a9406-125">Questa chiave viene generata quando il primo dispositivo fisico viene registrato con una risorsa.</span><span class="sxs-lookup"><span data-stu-id="a9406-125">This key is generated when the first physical device is registered with a resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9406-126">-SnapshotManagerPassword</span><span class="sxs-lookup"><span data-stu-id="a9406-126">-SnapshotManagerPassword</span></span>
<span data-ttu-id="a9406-127">Specifica la password di gestione snapshot.</span><span class="sxs-lookup"><span data-stu-id="a9406-127">Specifies the snapshot manager password.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9406-128">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="a9406-128">-TimeZone</span></span>
<span data-ttu-id="a9406-129">Specifica un fuso orario per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a9406-129">Specifies a time zone for the device.</span></span>
<span data-ttu-id="a9406-130">Puoi creare un oggetto **TimeZoneInfo** usando il metodo **GetSystemTimeZone ()** .</span><span class="sxs-lookup"><span data-stu-id="a9406-130">You can create a **TimeZoneInfo** object by using the **GetSystemTimeZone()** method.</span></span>
<span data-ttu-id="a9406-131">Ad esempio, questo comando crea un oggetto informazioni sul fuso orario per l'ora solare Pacifico: `\[System.TimeZoneInfo\]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }`</span><span class="sxs-lookup"><span data-stu-id="a9406-131">For example, this command creates a time zone information object for Pacific Standard Time: `\[System.TimeZoneInfo\]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }`</span></span>

```yaml
Type: TimeZoneInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9406-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9406-132">CommonParameters</span></span>
<span data-ttu-id="a9406-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9406-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9406-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9406-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9406-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a9406-135">INPUTS</span></span>

### <span data-ttu-id="a9406-136">TimeZoneInfo</span><span class="sxs-lookup"><span data-stu-id="a9406-136">TimeZoneInfo</span></span>
<span data-ttu-id="a9406-137">Puoi reindirizzare un oggetto **TimeZoneInfo** a questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9406-137">You can pipe a **TimeZoneInfo** object to this cmdlet.</span></span>

## <span data-ttu-id="a9406-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a9406-138">OUTPUTS</span></span>

### <span data-ttu-id="a9406-139">DeviceJobDetails</span><span class="sxs-lookup"><span data-stu-id="a9406-139">DeviceJobDetails</span></span>
<span data-ttu-id="a9406-140">Questo cmdlet restituisce i dettagli del dispositivo aggiornati per il dispositivo virtuale.</span><span class="sxs-lookup"><span data-stu-id="a9406-140">This cmdlet returns updated device details for the virtual device.</span></span>

## <span data-ttu-id="a9406-141">Note</span><span class="sxs-lookup"><span data-stu-id="a9406-141">NOTES</span></span>

## <span data-ttu-id="a9406-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a9406-142">RELATED LINKS</span></span>

[<span data-ttu-id="a9406-143">New-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="a9406-143">New-AzureStorSimpleVirtualDevice</span></span>](./New-AzureStorSimpleVirtualDevice.md)

[<span data-ttu-id="a9406-144">Set-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="a9406-144">Set-AzureStorSimpleDevice</span></span>](./Set-AzureStorSimpleDevice.md)



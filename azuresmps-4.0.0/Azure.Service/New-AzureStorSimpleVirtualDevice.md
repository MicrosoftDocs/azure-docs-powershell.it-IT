---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F16BCE0C-1F2C-4FB7-972D-28BE3CCD96D9
online version: ''
schema: 2.0.0
ms.openlocfilehash: dc41efa1901debf2efabf66f8d27f00da7eafe5f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023469"
---
# <span data-ttu-id="387d8-101">New-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="387d8-101">New-AzureStorSimpleVirtualDevice</span></span>

## <span data-ttu-id="387d8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="387d8-102">SYNOPSIS</span></span>
<span data-ttu-id="387d8-103">Crea un dispositivo StorSimple virtuale.</span><span class="sxs-lookup"><span data-stu-id="387d8-103">Creates a virtual StorSimple device.</span></span>

## <span data-ttu-id="387d8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="387d8-104">SYNTAX</span></span>

### <span data-ttu-id="387d8-105">CreateNewStorageAccount</span><span class="sxs-lookup"><span data-stu-id="387d8-105">CreateNewStorageAccount</span></span>
```
New-AzureStorSimpleVirtualDevice -VirtualDeviceName <String> -VirtualNetworkName <String> -SubNetName <String>
 [-StorageAccountName <String>] [-CreateNewStorageAccount] [-PersistAzureVMOnFailrue]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="387d8-106">UseExistingStorageAccount</span><span class="sxs-lookup"><span data-stu-id="387d8-106">UseExistingStorageAccount</span></span>
```
New-AzureStorSimpleVirtualDevice -VirtualDeviceName <String> -VirtualNetworkName <String> -SubNetName <String>
 -StorageAccountName <String> [-PersistAzureVMOnFailrue] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="387d8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="387d8-107">DESCRIPTION</span></span>
<span data-ttu-id="387d8-108">Il cmdlet **New-AzureStorSimpleVirtualDevice** crea un dispositivo StorSimple virtuale.</span><span class="sxs-lookup"><span data-stu-id="387d8-108">The **New-AzureStorSimpleVirtualDevice** cmdlet creates a virtual StorSimple device.</span></span>
<span data-ttu-id="387d8-109">Specificare un nome di dispositivo per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="387d8-109">Specify a device name for the device.</span></span>
<span data-ttu-id="387d8-110">Specificare i dettagli della rete virtuale e della subnet per la rete virtuale nello stesso abbonamento.</span><span class="sxs-lookup"><span data-stu-id="387d8-110">Specify virtual network and subnet details for the virtual network in the same subscription.</span></span>
<span data-ttu-id="387d8-111">La Geo deve corrispondere alla geo in cui viene creata la risorsa StorSimple.</span><span class="sxs-lookup"><span data-stu-id="387d8-111">The geo should match the geo in which the StorSimple resource is created.</span></span>
<span data-ttu-id="387d8-112">Per usare un account di archiviazione esistente per questo dispositivo virtuale, specificare il nome.</span><span class="sxs-lookup"><span data-stu-id="387d8-112">To use an existing storage account for this virtual device, specify the name.</span></span>
<span data-ttu-id="387d8-113">Per creare un nuovo account di archiviazione per il dispositivo virtuale, specificare i parametri *StorageAccountName* e *CreateNewStorageAccount* .</span><span class="sxs-lookup"><span data-stu-id="387d8-113">To create a new storage account for this virtual device, specify both the *StorageAccountName* and the *CreateNewStorageAccount* parameters.</span></span>

## <span data-ttu-id="387d8-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="387d8-114">EXAMPLES</span></span>

### <span data-ttu-id="387d8-115">Esempio 1: creare un dispositivo virtuale con un nuovo account e una rete esistente</span><span class="sxs-lookup"><span data-stu-id="387d8-115">Example 1: Create a virtual device with a new account and an existing network</span></span>
```
PS C:\>New-AzureStorSimpleVirtualDevice -VirtualDeviceName "Contosodevice02" -VirtualNetworkName "Saas2vpn" -SubNetName "TenantSubnet" -StorageAccountName "AzureTenant04" -CreateNewStorageAccount
64e4c564-b0ac-44b0-afb4-adf28ac24ad0
VERBOSE: The create job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId 64e4c564-b0ac-44b0-afb4-adf28ac24ad0 for tracking the job's status
```

<span data-ttu-id="387d8-116">Questo comando crea un dispositivo virtuale che usa un nuovo account di archiviazione e una rete virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="387d8-116">This command creates a virtual device that uses a new storage account and an existing virtual network.</span></span>

### <span data-ttu-id="387d8-117">Esempio 2: creare un dispositivo virtuale con un account esistente e una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="387d8-117">Example 2: Create a virtual device with an existing account and virtual network</span></span>
```
PS C:\>New-AzureStorSimpleVirtualDevice -VirtualDeviceName "ContosoDevice07" -VirtualNetworkName "Saas2vpn" -SubNetName TenantSubnet -StorageAccountName azurecisbvtdnd
2a18a3b7-1ec6-481d-b95d-66ba8f67ceaf
VERBOSE: The create job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId 2a18a3b7-1ec6-481d-b95d-66ba8f67ceaf for tracking the job's status
```

<span data-ttu-id="387d8-118">Questo comando crea un dispositivo virtuale che usa un account di archiviazione esistente e una rete virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="387d8-118">This command creates a virtual device that uses an existing storage account and an existing virtual network.</span></span>

## <span data-ttu-id="387d8-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="387d8-119">PARAMETERS</span></span>

### <span data-ttu-id="387d8-120">-CreateNewStorageAccount</span><span class="sxs-lookup"><span data-stu-id="387d8-120">-CreateNewStorageAccount</span></span>
<span data-ttu-id="387d8-121">Indica che questo cmdlet crea un nuovo account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="387d8-121">Indicates that this cmdlet creates a new storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateNewStorageAccount
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="387d8-122">-PersistAzureVMOnFailrue</span><span class="sxs-lookup"><span data-stu-id="387d8-122">-PersistAzureVMOnFailrue</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="387d8-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="387d8-123">-Profile</span></span>
<span data-ttu-id="387d8-124">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="387d8-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="387d8-125">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="387d8-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="387d8-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="387d8-126">-StorageAccountName</span></span>
<span data-ttu-id="387d8-127">Specifica il nome di un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="387d8-127">Specifies the name of a storage account.</span></span>

```yaml
Type: String
Parameter Sets: CreateNewStorageAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UseExistingStorageAccount
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="387d8-128">-SubNetname</span><span class="sxs-lookup"><span data-stu-id="387d8-128">-SubNetName</span></span>
<span data-ttu-id="387d8-129">Specifica il nome di una subnet virtuale.</span><span class="sxs-lookup"><span data-stu-id="387d8-129">Specifies the name of a virtual subnet.</span></span>

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

### <span data-ttu-id="387d8-130">-VirtualDeviceName</span><span class="sxs-lookup"><span data-stu-id="387d8-130">-VirtualDeviceName</span></span>
<span data-ttu-id="387d8-131">Specifica un nome per il dispositivo virtuale.</span><span class="sxs-lookup"><span data-stu-id="387d8-131">Specifies a name for the virtual device.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="387d8-132">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="387d8-132">-VirtualNetworkName</span></span>
<span data-ttu-id="387d8-133">Specifica il nome di una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="387d8-133">Specifies the name of a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VNetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="387d8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="387d8-134">CommonParameters</span></span>
<span data-ttu-id="387d8-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="387d8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="387d8-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="387d8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="387d8-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="387d8-137">INPUTS</span></span>

## <span data-ttu-id="387d8-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="387d8-138">OUTPUTS</span></span>

### <span data-ttu-id="387d8-139">Stringa</span><span class="sxs-lookup"><span data-stu-id="387d8-139">String</span></span>
<span data-ttu-id="387d8-140">Questo cmdlet restituisce l'ID del processo che crea il dispositivo virtuale.</span><span class="sxs-lookup"><span data-stu-id="387d8-140">This cmdlet returns the ID of the job that creates the virtual device.</span></span>
<span data-ttu-id="387d8-141">Puoi usare questo ID per tenere traccia dello stato di avanzamento usando il cmdlet Get-AzureStorSimpleJob.</span><span class="sxs-lookup"><span data-stu-id="387d8-141">You can use this ID to track the progress using the Get-AzureStorSimpleJob cmdlet.</span></span>

## <span data-ttu-id="387d8-142">Note</span><span class="sxs-lookup"><span data-stu-id="387d8-142">NOTES</span></span>

## <span data-ttu-id="387d8-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="387d8-143">RELATED LINKS</span></span>

[<span data-ttu-id="387d8-144">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="387d8-144">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="387d8-145">Set-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="387d8-145">Set-AzureStorSimpleVirtualDevice</span></span>](./Set-AzureStorSimpleVirtualDevice.md)



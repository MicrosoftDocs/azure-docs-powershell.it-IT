---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubmoduleconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
ms.openlocfilehash: 739153aebdaf8b089c0d180643056725a85f450a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987949"
---
# <span data-ttu-id="1dbf5-101">Get-AzIotHubModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="1dbf5-101">Get-AzIotHubModuleConnectionString</span></span>

## <span data-ttu-id="1dbf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dbf5-102">SYNOPSIS</span></span>
<span data-ttu-id="1dbf5-103">Ottenere la stringa di connessione di un modulo di dispositivo IoT di destinazione in un hub Iot.</span><span class="sxs-lookup"><span data-stu-id="1dbf5-103">Get the connection string of a target IoT device module in an Iot Hub.</span></span>

## <span data-ttu-id="1dbf5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1dbf5-104">SYNTAX</span></span>

### <span data-ttu-id="1dbf5-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1dbf5-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1dbf5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1dbf5-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleConnectionString [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1dbf5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1dbf5-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1dbf5-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1dbf5-108">DESCRIPTION</span></span>
<span data-ttu-id="1dbf5-109">Elencare la stringa di connessione di tutti i moduli o di un modulo specificato di un dispositivo IoT di destinazione contenuto in un hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="1dbf5-109">List connection string of all modules or a specified module of a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="1dbf5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1dbf5-110">EXAMPLES</span></span>

### <span data-ttu-id="1dbf5-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1dbf5-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Deviceid "myDevice1"

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******     
module2   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module2;x509=true
```

<span data-ttu-id="1dbf5-112">Mostra la stringa di connessione di tutti i moduli di un dispositivo IoT di destinazione in un hub Iot.</span><span class="sxs-lookup"><span data-stu-id="1dbf5-112">Show all modules connection string of a target IoT device in an Iot Hub.</span></span>

### <span data-ttu-id="1dbf5-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1dbf5-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubMCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "module1" -KeyType secondary

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******
```

<span data-ttu-id="1dbf5-114">Ottenere la stringa di connessione del modulo secondario di un dispositivo IoT di destinazione in un hub Iot.</span><span class="sxs-lookup"><span data-stu-id="1dbf5-114">Get the secondary module connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="1dbf5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1dbf5-115">PARAMETERS</span></span>

### <span data-ttu-id="1dbf5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dbf5-116">-DefaultProfile</span></span>
<span data-ttu-id="1dbf5-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1dbf5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dbf5-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="1dbf5-118">-DeviceId</span></span>
<span data-ttu-id="1dbf5-119">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1dbf5-119">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dbf5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1dbf5-120">-InputObject</span></span>
<span data-ttu-id="1dbf5-121">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="1dbf5-121">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1dbf5-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="1dbf5-122">-IotHubName</span></span>
<span data-ttu-id="1dbf5-123">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="1dbf5-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dbf5-124">-KeyType</span><span class="sxs-lookup"><span data-stu-id="1dbf5-124">-KeyType</span></span>
<span data-ttu-id="1dbf5-125">Tipo di chiave dei criteri di accesso condiviso per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="1dbf5-125">Shared access policy key type for auth.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSKeyType
Parameter Sets: (All)
Aliases:
Accepted values: primary, secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dbf5-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="1dbf5-126">-ModuleId</span></span>
<span data-ttu-id="1dbf5-127">ID modulo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1dbf5-127">Target Module Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dbf5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dbf5-128">-ResourceGroupName</span></span>
<span data-ttu-id="1dbf5-129">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="1dbf5-129">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dbf5-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1dbf5-130">-ResourceId</span></span>
<span data-ttu-id="1dbf5-131">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="1dbf5-131">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dbf5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dbf5-132">CommonParameters</span></span>
<span data-ttu-id="1dbf5-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dbf5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dbf5-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dbf5-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dbf5-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="1dbf5-135">INPUTS</span></span>

### <span data-ttu-id="1dbf5-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="1dbf5-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="1dbf5-137">System.String</span><span class="sxs-lookup"><span data-stu-id="1dbf5-137">System.String</span></span>

## <span data-ttu-id="1dbf5-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1dbf5-138">OUTPUTS</span></span>

### <span data-ttu-id="1dbf5-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="1dbf5-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleConnectionString</span></span>

## <span data-ttu-id="1dbf5-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="1dbf5-140">NOTES</span></span>

## <span data-ttu-id="1dbf5-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1dbf5-141">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmoduleconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
ms.openlocfilehash: 30926eaad6447f109b1755d419be0b3931a76054
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348091"
---
# <span data-ttu-id="0f053-101">Get-AzIotHubModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="0f053-101">Get-AzIotHubModuleConnectionString</span></span>

## <span data-ttu-id="0f053-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0f053-102">SYNOPSIS</span></span>
<span data-ttu-id="0f053-103">Ottenere la stringa di connessione di un modulo di dispositivo di un sacco di destinazione in un hub molto.</span><span class="sxs-lookup"><span data-stu-id="0f053-103">Get the connection string of a target IoT device module in an Iot Hub.</span></span>

## <span data-ttu-id="0f053-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f053-104">SYNTAX</span></span>

### <span data-ttu-id="0f053-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0f053-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f053-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0f053-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleConnectionString [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f053-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0f053-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f053-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f053-108">DESCRIPTION</span></span>
<span data-ttu-id="0f053-109">Elenca la stringa di connessione di tutti i moduli o un modulo specificato di un dispositivo di destinazione per gli altri contenuti in un hub di Azure.</span><span class="sxs-lookup"><span data-stu-id="0f053-109">List connection string of all modules or a specified module of a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="0f053-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f053-110">EXAMPLES</span></span>

### <span data-ttu-id="0f053-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0f053-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Deviceid "myDevice1"

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******     
module2   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module2;x509=true
```

<span data-ttu-id="0f053-112">Mostra tutta la stringa di connessione dei moduli di un dispositivo di destinazione in un hub molto.</span><span class="sxs-lookup"><span data-stu-id="0f053-112">Show all modules connection string of a target IoT device in an Iot Hub.</span></span>

### <span data-ttu-id="0f053-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0f053-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubMCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "module1" -KeyType secondary

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******
```

<span data-ttu-id="0f053-114">Ottieni la stringa di connessione del modulo secondario di un dispositivo di destinazione in un hub molto.</span><span class="sxs-lookup"><span data-stu-id="0f053-114">Get the secondary module connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="0f053-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0f053-115">PARAMETERS</span></span>

### <span data-ttu-id="0f053-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f053-116">-DefaultProfile</span></span>
<span data-ttu-id="0f053-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0f053-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f053-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="0f053-118">-DeviceId</span></span>
<span data-ttu-id="0f053-119">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0f053-119">Target Device Id.</span></span>

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

### <span data-ttu-id="0f053-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f053-120">-InputObject</span></span>
<span data-ttu-id="0f053-121">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="0f053-121">IotHub object</span></span>

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

### <span data-ttu-id="0f053-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="0f053-122">-IotHubName</span></span>
<span data-ttu-id="0f053-123">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="0f053-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="0f053-124">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="0f053-124">-KeyType</span></span>
<span data-ttu-id="0f053-125">Tipo di chiave dei criteri di accesso condiviso per auth.</span><span class="sxs-lookup"><span data-stu-id="0f053-125">Shared access policy key type for auth.</span></span>

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

### <span data-ttu-id="0f053-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="0f053-126">-ModuleId</span></span>
<span data-ttu-id="0f053-127">ID modulo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0f053-127">Target Module Id.</span></span>

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

### <span data-ttu-id="0f053-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f053-128">-ResourceGroupName</span></span>
<span data-ttu-id="0f053-129">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="0f053-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0f053-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f053-130">-ResourceId</span></span>
<span data-ttu-id="0f053-131">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="0f053-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="0f053-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f053-132">CommonParameters</span></span>
<span data-ttu-id="0f053-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f053-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f053-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f053-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f053-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0f053-135">INPUTS</span></span>

### <span data-ttu-id="0f053-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="0f053-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="0f053-137">System. String</span><span class="sxs-lookup"><span data-stu-id="0f053-137">System.String</span></span>

## <span data-ttu-id="0f053-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f053-138">OUTPUTS</span></span>

### <span data-ttu-id="0f053-139">Microsoft. Azure. Commands. Management. IotHub. Models. PSModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="0f053-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleConnectionString</span></span>

## <span data-ttu-id="0f053-140">Note</span><span class="sxs-lookup"><span data-stu-id="0f053-140">NOTES</span></span>

## <span data-ttu-id="0f053-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f053-141">RELATED LINKS</span></span>

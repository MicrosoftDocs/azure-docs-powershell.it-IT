---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
ms.openlocfilehash: 616fface9f20609c043884754e9b3904ffc83e67
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188230"
---
# <span data-ttu-id="3e287-101">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e287-101">Get-AzIotHubConfiguration</span></span>

## <span data-ttu-id="3e287-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e287-102">SYNOPSIS</span></span>
<span data-ttu-id="3e287-103">Elenco di tutte le configurazioni automatiche di gestione dei dispositivi IoT o di una particolare configurazione.</span><span class="sxs-lookup"><span data-stu-id="3e287-103">Lists all or a particular IoT automatic device management configuration.</span></span>

## <span data-ttu-id="3e287-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e287-104">SYNTAX</span></span>

### <span data-ttu-id="3e287-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3e287-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e287-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3e287-106">InputObjectSet</span></span>
```
Get-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e287-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3e287-107">ResourceIdSet</span></span>
```
Get-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e287-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3e287-108">DESCRIPTION</span></span>
<span data-ttu-id="3e287-109">Ottenere i dettagli di una configurazione automatica di gestione dei dispositivi IoT o elencare le configurazioni di gestione automatica dei dispositivi IoT in un Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="3e287-109">Get the details of an IoT automatic device management configuration or list IoT automatic device management configurations in an IoT Hub.</span></span>
<span data-ttu-id="3e287-110">Per https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management altre informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="3e287-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="3e287-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e287-111">EXAMPLES</span></span>

### <span data-ttu-id="3e287-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3e287-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="3e287-113">Ottenere i dettagli di una configurazione automatica di gestione dei dispositivi IoT.</span><span class="sxs-lookup"><span data-stu-id="3e287-113">Get the details of an IoT automatic device management configuration.</span></span>

### <span data-ttu-id="3e287-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3e287-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="3e287-115">Elencare le configurazioni automatiche di gestione dei dispositivi IoT in un Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="3e287-115">List IoT automatic device management configurations in an IoT Hub.</span></span>

## <span data-ttu-id="3e287-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e287-116">PARAMETERS</span></span>

### <span data-ttu-id="3e287-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e287-117">-DefaultProfile</span></span>
<span data-ttu-id="3e287-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3e287-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e287-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e287-119">-InputObject</span></span>
<span data-ttu-id="3e287-120">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="3e287-120">IotHub object</span></span>

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

### <span data-ttu-id="3e287-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="3e287-121">-IotHubName</span></span>
<span data-ttu-id="3e287-122">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="3e287-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="3e287-123">-Name</span><span class="sxs-lookup"><span data-stu-id="3e287-123">-Name</span></span>
<span data-ttu-id="3e287-124">Identificatore della configurazione.</span><span class="sxs-lookup"><span data-stu-id="3e287-124">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="3e287-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e287-125">-ResourceGroupName</span></span>
<span data-ttu-id="3e287-126">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="3e287-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3e287-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e287-127">-ResourceId</span></span>
<span data-ttu-id="3e287-128">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="3e287-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="3e287-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e287-129">CommonParameters</span></span>
<span data-ttu-id="3e287-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e287-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e287-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e287-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e287-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="3e287-132">INPUTS</span></span>

### <span data-ttu-id="3e287-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="3e287-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="3e287-134">System.String</span><span class="sxs-lookup"><span data-stu-id="3e287-134">System.String</span></span>

## <span data-ttu-id="3e287-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e287-135">OUTPUTS</span></span>

### <span data-ttu-id="3e287-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e287-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

### <span data-ttu-id="3e287-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurations[]</span><span class="sxs-lookup"><span data-stu-id="3e287-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurations[]</span></span>

## <span data-ttu-id="3e287-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="3e287-138">NOTES</span></span>

## <span data-ttu-id="3e287-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e287-139">RELATED LINKS</span></span>

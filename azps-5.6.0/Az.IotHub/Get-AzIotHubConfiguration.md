---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
ms.openlocfilehash: b50d0b493243a07632403890d0324fefaba7dc8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988118"
---
# <span data-ttu-id="4eb99-101">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="4eb99-101">Get-AzIotHubConfiguration</span></span>

## <span data-ttu-id="4eb99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4eb99-102">SYNOPSIS</span></span>
<span data-ttu-id="4eb99-103">Elenco di tutte le configurazioni automatiche di gestione dei dispositivi IoT o di una particolare configurazione.</span><span class="sxs-lookup"><span data-stu-id="4eb99-103">Lists all or a particular IoT automatic device management configuration.</span></span>

## <span data-ttu-id="4eb99-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4eb99-104">SYNTAX</span></span>

### <span data-ttu-id="4eb99-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4eb99-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4eb99-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4eb99-106">InputObjectSet</span></span>
```
Get-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4eb99-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4eb99-107">ResourceIdSet</span></span>
```
Get-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4eb99-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4eb99-108">DESCRIPTION</span></span>
<span data-ttu-id="4eb99-109">Ottenere i dettagli di una configurazione automatica di gestione dei dispositivi IoT o elencare le configurazioni di gestione automatica dei dispositivi IoT in un Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="4eb99-109">Get the details of an IoT automatic device management configuration or list IoT automatic device management configurations in an IoT Hub.</span></span>
<span data-ttu-id="4eb99-110">Per https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management altre informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="4eb99-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="4eb99-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4eb99-111">EXAMPLES</span></span>

### <span data-ttu-id="4eb99-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4eb99-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="4eb99-113">Ottenere i dettagli di una configurazione automatica di gestione dei dispositivi IoT.</span><span class="sxs-lookup"><span data-stu-id="4eb99-113">Get the details of an IoT automatic device management configuration.</span></span>

### <span data-ttu-id="4eb99-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4eb99-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="4eb99-115">Elencare le configurazioni automatiche di gestione dei dispositivi IoT in un Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="4eb99-115">List IoT automatic device management configurations in an IoT Hub.</span></span>

## <span data-ttu-id="4eb99-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4eb99-116">PARAMETERS</span></span>

### <span data-ttu-id="4eb99-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eb99-117">-DefaultProfile</span></span>
<span data-ttu-id="4eb99-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4eb99-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4eb99-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4eb99-119">-InputObject</span></span>
<span data-ttu-id="4eb99-120">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="4eb99-120">IotHub object</span></span>

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

### <span data-ttu-id="4eb99-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="4eb99-121">-IotHubName</span></span>
<span data-ttu-id="4eb99-122">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="4eb99-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4eb99-123">-Name</span><span class="sxs-lookup"><span data-stu-id="4eb99-123">-Name</span></span>
<span data-ttu-id="4eb99-124">Identificatore della configurazione.</span><span class="sxs-lookup"><span data-stu-id="4eb99-124">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="4eb99-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4eb99-125">-ResourceGroupName</span></span>
<span data-ttu-id="4eb99-126">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="4eb99-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4eb99-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4eb99-127">-ResourceId</span></span>
<span data-ttu-id="4eb99-128">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="4eb99-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="4eb99-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eb99-129">CommonParameters</span></span>
<span data-ttu-id="4eb99-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4eb99-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eb99-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4eb99-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eb99-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="4eb99-132">INPUTS</span></span>

### <span data-ttu-id="4eb99-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="4eb99-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="4eb99-134">System.String</span><span class="sxs-lookup"><span data-stu-id="4eb99-134">System.String</span></span>

## <span data-ttu-id="4eb99-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4eb99-135">OUTPUTS</span></span>

### <span data-ttu-id="4eb99-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="4eb99-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

### <span data-ttu-id="4eb99-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurations[]</span><span class="sxs-lookup"><span data-stu-id="4eb99-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurations[]</span></span>

## <span data-ttu-id="4eb99-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="4eb99-138">NOTES</span></span>

## <span data-ttu-id="4eb99-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4eb99-139">RELATED LINKS</span></span>

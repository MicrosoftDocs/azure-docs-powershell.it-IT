---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
ms.openlocfilehash: 616fface9f20609c043884754e9b3904ffc83e67
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191325"
---
# <span data-ttu-id="0b154-101">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b154-101">Get-AzIotHubConfiguration</span></span>

## <span data-ttu-id="0b154-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0b154-102">SYNOPSIS</span></span>
<span data-ttu-id="0b154-103">Elenca tutti o una particolare configurazione della gestione automatica dei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="0b154-103">Lists all or a particular IoT automatic device management configuration.</span></span>

## <span data-ttu-id="0b154-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0b154-104">SYNTAX</span></span>

### <span data-ttu-id="0b154-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0b154-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b154-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0b154-106">InputObjectSet</span></span>
```
Get-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b154-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0b154-107">ResourceIdSet</span></span>
```
Get-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b154-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b154-108">DESCRIPTION</span></span>
<span data-ttu-id="0b154-109">Ottenere i dettagli di una configurazione automatica per la gestione di dispositivi automatici o un elenco di configurazioni per la gestione di dispositivi automatici in un hub molto.</span><span class="sxs-lookup"><span data-stu-id="0b154-109">Get the details of an IoT automatic device management configuration or list IoT automatic device management configurations in an IoT Hub.</span></span>
<span data-ttu-id="0b154-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-managementPer altre informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="0b154-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="0b154-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0b154-111">EXAMPLES</span></span>

### <span data-ttu-id="0b154-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0b154-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="0b154-113">Ottenere i dettagli di una configurazione di gestione automatica dei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="0b154-113">Get the details of an IoT automatic device management configuration.</span></span>

### <span data-ttu-id="0b154-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0b154-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="0b154-115">Elenco delle configurazioni automatiche per la gestione dei dispositivi in un hub molto.</span><span class="sxs-lookup"><span data-stu-id="0b154-115">List IoT automatic device management configurations in an IoT Hub.</span></span>

## <span data-ttu-id="0b154-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0b154-116">PARAMETERS</span></span>

### <span data-ttu-id="0b154-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b154-117">-DefaultProfile</span></span>
<span data-ttu-id="0b154-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0b154-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b154-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b154-119">-InputObject</span></span>
<span data-ttu-id="0b154-120">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="0b154-120">IotHub object</span></span>

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

### <span data-ttu-id="0b154-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="0b154-121">-IotHubName</span></span>
<span data-ttu-id="0b154-122">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="0b154-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="0b154-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="0b154-123">-Name</span></span>
<span data-ttu-id="0b154-124">Identificatore per la configurazione.</span><span class="sxs-lookup"><span data-stu-id="0b154-124">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="0b154-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b154-125">-ResourceGroupName</span></span>
<span data-ttu-id="0b154-126">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="0b154-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0b154-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b154-127">-ResourceId</span></span>
<span data-ttu-id="0b154-128">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="0b154-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="0b154-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b154-129">CommonParameters</span></span>
<span data-ttu-id="0b154-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b154-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b154-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b154-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b154-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0b154-132">INPUTS</span></span>

### <span data-ttu-id="0b154-133">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="0b154-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="0b154-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0b154-134">System.String</span></span>

## <span data-ttu-id="0b154-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0b154-135">OUTPUTS</span></span>

### <span data-ttu-id="0b154-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b154-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

### <span data-ttu-id="0b154-137">Microsoft. Azure. Commands. Management. IotHub. Models. PSConfigurations []</span><span class="sxs-lookup"><span data-stu-id="0b154-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurations[]</span></span>

## <span data-ttu-id="0b154-138">Note</span><span class="sxs-lookup"><span data-stu-id="0b154-138">NOTES</span></span>

## <span data-ttu-id="0b154-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0b154-139">RELATED LINKS</span></span>
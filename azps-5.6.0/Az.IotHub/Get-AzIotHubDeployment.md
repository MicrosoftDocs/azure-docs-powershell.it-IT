---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
ms.openlocfilehash: 4c4a9259f80360cfa8947035e84368ca18ed77d0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988104"
---
# <span data-ttu-id="8b465-101">Get-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="8b465-101">Get-AzIotHubDeployment</span></span>

## <span data-ttu-id="8b465-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b465-102">SYNOPSIS</span></span>
<span data-ttu-id="8b465-103">Elenca tutte le distribuzioni Edge IoT o una particolare.</span><span class="sxs-lookup"><span data-stu-id="8b465-103">Lists all or a particular IoT Edge deployment.</span></span>

## <span data-ttu-id="8b465-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8b465-104">SYNTAX</span></span>

### <span data-ttu-id="8b465-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8b465-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b465-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8b465-106">InputObjectSet</span></span>
```
Get-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8b465-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8b465-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8b465-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8b465-108">DESCRIPTION</span></span>
<span data-ttu-id="8b465-109">Ottenere i dettagli di una distribuzione Edge IoT o elencare le distribuzioni Edge IoT in un Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="8b465-109">Get the details of an IoT Edge deployment or List IoT Edge deployments in an IoT Hub.</span></span>
<span data-ttu-id="8b465-110">Per https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring altre informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="8b465-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="8b465-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8b465-111">EXAMPLES</span></span>

### <span data-ttu-id="8b465-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8b465-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="8b465-113">Ottenere i dettagli di una distribuzione Edge IoT.</span><span class="sxs-lookup"><span data-stu-id="8b465-113">Get the details of an IoT Edge deployment.</span></span>

### <span data-ttu-id="8b465-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8b465-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="8b465-115">Elencare tutte le distribuzioni Edge IoT in un Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="8b465-115">List all IoT Edge deployments in an IoT Hub.</span></span>

## <span data-ttu-id="8b465-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b465-116">PARAMETERS</span></span>

### <span data-ttu-id="8b465-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b465-117">-DefaultProfile</span></span>
<span data-ttu-id="8b465-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8b465-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b465-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b465-119">-InputObject</span></span>
<span data-ttu-id="8b465-120">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="8b465-120">IotHub object</span></span>

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

### <span data-ttu-id="8b465-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="8b465-121">-IotHubName</span></span>
<span data-ttu-id="8b465-122">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="8b465-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="8b465-123">-Name</span><span class="sxs-lookup"><span data-stu-id="8b465-123">-Name</span></span>
<span data-ttu-id="8b465-124">Identificatore per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="8b465-124">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="8b465-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b465-125">-ResourceGroupName</span></span>
<span data-ttu-id="8b465-126">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="8b465-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8b465-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b465-127">-ResourceId</span></span>
<span data-ttu-id="8b465-128">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="8b465-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="8b465-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b465-129">CommonParameters</span></span>
<span data-ttu-id="8b465-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b465-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b465-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b465-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b465-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="8b465-132">INPUTS</span></span>

### <span data-ttu-id="8b465-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8b465-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8b465-134">System.String</span><span class="sxs-lookup"><span data-stu-id="8b465-134">System.String</span></span>

## <span data-ttu-id="8b465-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8b465-135">OUTPUTS</span></span>

### <span data-ttu-id="8b465-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="8b465-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

### <span data-ttu-id="8b465-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments[]</span><span class="sxs-lookup"><span data-stu-id="8b465-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments[]</span></span>

## <span data-ttu-id="8b465-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="8b465-138">NOTES</span></span>

## <span data-ttu-id="8b465-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8b465-139">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
ms.openlocfilehash: 1440b77d753a27b1c2a7176be5b44ef69fca2e50
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329995"
---
# <span data-ttu-id="d1370-101">Get-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="d1370-101">Get-AzIotHubDeployment</span></span>

## <span data-ttu-id="d1370-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d1370-102">SYNOPSIS</span></span>
<span data-ttu-id="d1370-103">Elenca tutte le distribuzioni di Edge o una particolare distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d1370-103">Lists all or a particular IoT Edge deployment.</span></span>

## <span data-ttu-id="d1370-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1370-104">SYNTAX</span></span>

### <span data-ttu-id="d1370-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d1370-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1370-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d1370-106">InputObjectSet</span></span>
```
Get-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d1370-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d1370-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1370-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1370-108">DESCRIPTION</span></span>
<span data-ttu-id="d1370-109">Ottenere i dettagli di una distribuzione Edge molto o di un elenco di distribuzioni Edge molto in un hub molto.</span><span class="sxs-lookup"><span data-stu-id="d1370-109">Get the details of an IoT Edge deployment or List IoT Edge deployments in an IoT Hub.</span></span>
<span data-ttu-id="d1370-110"> https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoringPer altre informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="d1370-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="d1370-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1370-111">EXAMPLES</span></span>

### <span data-ttu-id="d1370-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d1370-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="d1370-113">Ottenere i dettagli di una distribuzione di Edge molto.</span><span class="sxs-lookup"><span data-stu-id="d1370-113">Get the details of an IoT Edge deployment.</span></span>

### <span data-ttu-id="d1370-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d1370-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="d1370-115">Elencare tutte le distribuzioni di Edge molto in un hub molto.</span><span class="sxs-lookup"><span data-stu-id="d1370-115">List all IoT Edge deployments in an IoT Hub.</span></span>

## <span data-ttu-id="d1370-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d1370-116">PARAMETERS</span></span>

### <span data-ttu-id="d1370-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1370-117">-DefaultProfile</span></span>
<span data-ttu-id="d1370-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d1370-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1370-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1370-119">-InputObject</span></span>
<span data-ttu-id="d1370-120">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="d1370-120">IotHub object</span></span>

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

### <span data-ttu-id="d1370-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="d1370-121">-IotHubName</span></span>
<span data-ttu-id="d1370-122">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="d1370-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d1370-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="d1370-123">-Name</span></span>
<span data-ttu-id="d1370-124">Identificatore per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d1370-124">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="d1370-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1370-125">-ResourceGroupName</span></span>
<span data-ttu-id="d1370-126">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d1370-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d1370-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1370-127">-ResourceId</span></span>
<span data-ttu-id="d1370-128">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="d1370-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d1370-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1370-129">CommonParameters</span></span>
<span data-ttu-id="d1370-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1370-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1370-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1370-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1370-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d1370-132">INPUTS</span></span>

### <span data-ttu-id="d1370-133">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d1370-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d1370-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d1370-134">System.String</span></span>

## <span data-ttu-id="d1370-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1370-135">OUTPUTS</span></span>

### <span data-ttu-id="d1370-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDEPLOYMENT</span><span class="sxs-lookup"><span data-stu-id="d1370-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

### <span data-ttu-id="d1370-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments []</span><span class="sxs-lookup"><span data-stu-id="d1370-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments[]</span></span>

## <span data-ttu-id="d1370-138">Note</span><span class="sxs-lookup"><span data-stu-id="d1370-138">NOTES</span></span>

## <span data-ttu-id="d1370-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1370-139">RELATED LINKS</span></span>

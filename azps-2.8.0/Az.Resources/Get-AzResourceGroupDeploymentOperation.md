---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
ms.openlocfilehash: a67bfb43aa4cafe4b9c7f20e6ff757989deee5d6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854878"
---
# <span data-ttu-id="d4feb-101">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d4feb-101">Get-AzResourceGroupDeploymentOperation</span></span>

## <span data-ttu-id="d4feb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d4feb-102">SYNOPSIS</span></span>
<span data-ttu-id="d4feb-103">Ottiene l'operazione di distribuzione del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d4feb-103">Gets the resource group deployment operation</span></span>

## <span data-ttu-id="d4feb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d4feb-104">SYNTAX</span></span>

```
Get-AzResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d4feb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d4feb-105">DESCRIPTION</span></span>
<span data-ttu-id="d4feb-106">Il cmdlet **Get-AzResourceGroupDeploymentOperation** elenca tutte le operazioni che facevano parte di una distribuzione per identificare e fornire ulteriori informazioni sulle operazioni esatte non riuscite per una specifica distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d4feb-106">The **Get-AzResourceGroupDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="d4feb-107">Può anche visualizzare la risposta e il contenuto della richiesta per ogni operazione di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d4feb-107">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="d4feb-108">Queste sono le stesse informazioni fornite nei dettagli di distribuzione nel portale.</span><span class="sxs-lookup"><span data-stu-id="d4feb-108">This is the same information provided in the deployment details on the portal.</span></span>
<span data-ttu-id="d4feb-109">Per ottenere la richiesta e il contenuto della risposta, abilitare l'impostazione quando si invia una distribuzione tramite **New-AzResourceGroupDeployment**.</span><span class="sxs-lookup"><span data-stu-id="d4feb-109">To get the request and the response content, enable the setting when submitting a deployment through **New-AzResourceGroupDeployment**.</span></span>
<span data-ttu-id="d4feb-110">Può potenzialmente registrare e esporre segreti come le password usate nella proprietà Resource o le operazioni di **listKeys** che vengono quindi restituite quando recuperi le operazioni di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d4feb-110">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="d4feb-111">Per altre informazioni su questa impostazione e su come abilitarla, vedere New-AzResourceGroupDeployment e debug delle distribuzioni del modello ARM</span><span class="sxs-lookup"><span data-stu-id="d4feb-111">For more on this setting and how to enable it, see New-AzResourceGroupDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="d4feb-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d4feb-112">EXAMPLES</span></span>

### <span data-ttu-id="d4feb-113">Get1</span><span class="sxs-lookup"><span data-stu-id="d4feb-113">Get1</span></span>
```
PS C:\>Get-AzResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

<span data-ttu-id="d4feb-114">Ottiene l'operazione di distribuzione con il nome "test" in gruppo risorse "test"</span><span class="sxs-lookup"><span data-stu-id="d4feb-114">Gets deployment operation with name "test" under resource group "test"</span></span>

## <span data-ttu-id="d4feb-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d4feb-115">PARAMETERS</span></span>

### <span data-ttu-id="d4feb-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d4feb-116">-ApiVersion</span></span>
<span data-ttu-id="d4feb-117">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="d4feb-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="d4feb-118">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="d4feb-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="d4feb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4feb-119">-DefaultProfile</span></span>
<span data-ttu-id="d4feb-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d4feb-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4feb-121">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="d4feb-121">-DeploymentName</span></span>
<span data-ttu-id="d4feb-122">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d4feb-122">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4feb-123">-Pre</span><span class="sxs-lookup"><span data-stu-id="d4feb-123">-Pre</span></span>
<span data-ttu-id="d4feb-124">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="d4feb-124">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4feb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4feb-125">-ResourceGroupName</span></span>
<span data-ttu-id="d4feb-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d4feb-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4feb-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d4feb-127">-SubscriptionId</span></span>
<span data-ttu-id="d4feb-128">La sottoscrizione da usare.</span><span class="sxs-lookup"><span data-stu-id="d4feb-128">The subscription to use.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4feb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4feb-129">CommonParameters</span></span>
<span data-ttu-id="d4feb-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4feb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4feb-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4feb-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4feb-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d4feb-132">INPUTS</span></span>

### <span data-ttu-id="d4feb-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d4feb-133">System.String</span></span>

### <span data-ttu-id="d4feb-134">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d4feb-134">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d4feb-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d4feb-135">OUTPUTS</span></span>

### <span data-ttu-id="d4feb-136">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="d4feb-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d4feb-137">Note</span><span class="sxs-lookup"><span data-stu-id="d4feb-137">NOTES</span></span>

## <span data-ttu-id="d4feb-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d4feb-138">RELATED LINKS</span></span>

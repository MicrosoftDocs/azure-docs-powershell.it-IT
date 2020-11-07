---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroupdeploymentoperation
schema: 2.0.0
ms.openlocfilehash: 545047eea1451d5c03bba9db805c1d5a1a928e08
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866430"
---
# <span data-ttu-id="ef6ca-101">Get-AzureRmResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="ef6ca-101">Get-AzureRmResourceGroupDeploymentOperation</span></span>

## <span data-ttu-id="ef6ca-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ef6ca-102">SYNOPSIS</span></span>
<span data-ttu-id="ef6ca-103">Ottiene l'operazione di distribuzione del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ef6ca-103">Gets the resource group deployment operation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef6ca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ef6ca-104">SYNTAX</span></span>

```
Get-AzureRmResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ef6ca-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef6ca-105">DESCRIPTION</span></span>
<span data-ttu-id="ef6ca-106">Il cmdlet **Get-AzureRmResourceGroupDeploymentOperation** elenca tutte le operazioni che facevano parte di una distribuzione per identificare e fornire ulteriori informazioni sulle operazioni esatte non riuscite per una specifica distribuzione.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-106">The **Get-AzureRmResourceGroupDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="ef6ca-107">Può anche visualizzare la risposta e il contenuto della richiesta per ogni operazione di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-107">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="ef6ca-108">Queste sono le stesse informazioni fornite nei dettagli di distribuzione nel portale.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-108">This is the same information provided in the deployment details on the portal.</span></span>
<span data-ttu-id="ef6ca-109">Per ottenere la richiesta e il contenuto della risposta, abilitare l'impostazione quando si invia una distribuzione tramite **New-AzureRmResourceGroupDeployment**.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-109">To get the request and the response content, enable the setting when submitting a deployment through **New-AzureRmResourceGroupDeployment**.</span></span>
<span data-ttu-id="ef6ca-110">Può potenzialmente registrare e esporre segreti come le password usate nella proprietà Resource o le operazioni di **listKeys** che vengono quindi restituite quando recuperi le operazioni di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-110">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="ef6ca-111">Per altre informazioni su questa impostazione e su come abilitarla, vedere New-AzureRmResourceGroupDeployment e debug delle distribuzioni del modello ARM</span><span class="sxs-lookup"><span data-stu-id="ef6ca-111">For more on this setting and how to enable it, see New-AzureRmResourceGroupDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="ef6ca-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ef6ca-112">EXAMPLES</span></span>

### <span data-ttu-id="ef6ca-113">Get1</span><span class="sxs-lookup"><span data-stu-id="ef6ca-113">Get1</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

<span data-ttu-id="ef6ca-114">Ottiene l'operazione di distribuzione con il nome "test" in gruppo risorse "test"</span><span class="sxs-lookup"><span data-stu-id="ef6ca-114">Gets deployment operation with name "test" under resource group "test"</span></span>

## <span data-ttu-id="ef6ca-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ef6ca-115">PARAMETERS</span></span>

### <span data-ttu-id="ef6ca-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ef6ca-116">-ApiVersion</span></span>
<span data-ttu-id="ef6ca-117">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="ef6ca-118">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="ef6ca-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef6ca-119">-DefaultProfile</span></span>
<span data-ttu-id="ef6ca-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ef6ca-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6ca-121">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="ef6ca-121">-DeploymentName</span></span>
<span data-ttu-id="ef6ca-122">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-122">The deployment name.</span></span>

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

### <span data-ttu-id="ef6ca-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ef6ca-123">-InformationAction</span></span>
<span data-ttu-id="ef6ca-124">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-124">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="ef6ca-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ef6ca-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ef6ca-126">Continuare</span><span class="sxs-lookup"><span data-stu-id="ef6ca-126">Continue</span></span>
- <span data-ttu-id="ef6ca-127">Ignora</span><span class="sxs-lookup"><span data-stu-id="ef6ca-127">Ignore</span></span>
- <span data-ttu-id="ef6ca-128">Informarsi</span><span class="sxs-lookup"><span data-stu-id="ef6ca-128">Inquire</span></span>
- <span data-ttu-id="ef6ca-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ef6ca-129">SilentlyContinue</span></span>
- <span data-ttu-id="ef6ca-130">Stop</span><span class="sxs-lookup"><span data-stu-id="ef6ca-130">Stop</span></span>
- <span data-ttu-id="ef6ca-131">Sospensione</span><span class="sxs-lookup"><span data-stu-id="ef6ca-131">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6ca-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ef6ca-132">-InformationVariable</span></span>
<span data-ttu-id="ef6ca-133">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-133">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6ca-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="ef6ca-134">-Pre</span></span>
<span data-ttu-id="ef6ca-135">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ef6ca-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef6ca-136">-ResourceGroupName</span></span>
<span data-ttu-id="ef6ca-137">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-137">The resource group name.</span></span>

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

### <span data-ttu-id="ef6ca-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ef6ca-138">-SubscriptionId</span></span>
<span data-ttu-id="ef6ca-139">La sottoscrizione da usare.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-139">The subscription to use.</span></span>

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

### <span data-ttu-id="ef6ca-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef6ca-140">CommonParameters</span></span>
<span data-ttu-id="ef6ca-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef6ca-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef6ca-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef6ca-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ef6ca-143">INPUTS</span></span>

## <span data-ttu-id="ef6ca-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ef6ca-144">OUTPUTS</span></span>

## <span data-ttu-id="ef6ca-145">Note</span><span class="sxs-lookup"><span data-stu-id="ef6ca-145">NOTES</span></span>

## <span data-ttu-id="ef6ca-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ef6ca-146">RELATED LINKS</span></span>

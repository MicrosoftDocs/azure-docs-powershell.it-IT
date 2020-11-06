---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeploymentOperation.md
ms.openlocfilehash: 557aa312200a2e5c49e33f8a176079ee4b27b629
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512356"
---
# <span data-ttu-id="a7ac2-101">Get-AzureRmResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="a7ac2-101">Get-AzureRmResourceGroupDeploymentOperation</span></span>

## <span data-ttu-id="a7ac2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a7ac2-102">SYNOPSIS</span></span>
<span data-ttu-id="a7ac2-103">Ottiene l'operazione di distribuzione del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a7ac2-103">Gets the resource group deployment operation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7ac2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a7ac2-104">SYNTAX</span></span>

```
Get-AzureRmResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a7ac2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7ac2-105">DESCRIPTION</span></span>
<span data-ttu-id="a7ac2-106">Il cmdlet **Get-AzureRmResourceGroupDeploymentOperation** elenca tutte le operazioni che facevano parte di una distribuzione per identificare e fornire ulteriori informazioni sulle operazioni esatte non riuscite per una specifica distribuzione.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-106">The **Get-AzureRmResourceGroupDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="a7ac2-107">Può anche visualizzare la risposta e il contenuto della richiesta per ogni operazione di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-107">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="a7ac2-108">Queste sono le stesse informazioni fornite nei dettagli di distribuzione nel portale.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-108">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="a7ac2-109">Per ottenere la richiesta e il contenuto della risposta, abilitare l'impostazione quando si invia una distribuzione tramite **New-AzureRmResourceGroupDeployment**.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-109">To get the request and the response content, enable the setting when submitting a deployment through **New-AzureRmResourceGroupDeployment**.</span></span>
<span data-ttu-id="a7ac2-110">Può potenzialmente registrare e esporre segreti come le password usate nella proprietà Resource o le operazioni di **listKeys** che vengono quindi restituite quando recuperi le operazioni di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-110">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="a7ac2-111">Per altre informazioni su questa impostazione e su come abilitarla, vedere New-AzureRmResourceGroupDeployment e debug delle distribuzioni del modello ARM</span><span class="sxs-lookup"><span data-stu-id="a7ac2-111">For more on this setting and how to enable it, see New-AzureRmResourceGroupDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="a7ac2-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a7ac2-112">EXAMPLES</span></span>

### <span data-ttu-id="a7ac2-113">Get1</span><span class="sxs-lookup"><span data-stu-id="a7ac2-113">Get1</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

<span data-ttu-id="a7ac2-114">Ottiene l'operazione di distribuzione con il nome "test" in gruppo risorse "test"</span><span class="sxs-lookup"><span data-stu-id="a7ac2-114">Gets deployment operation with name "test" under resource group "test"</span></span>

## <span data-ttu-id="a7ac2-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a7ac2-115">PARAMETERS</span></span>

### <span data-ttu-id="a7ac2-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a7ac2-116">-ApiVersion</span></span>
<span data-ttu-id="a7ac2-117">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="a7ac2-118">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-118">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7ac2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7ac2-119">-DefaultProfile</span></span>
<span data-ttu-id="a7ac2-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a7ac2-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7ac2-121">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="a7ac2-121">-DeploymentName</span></span>
<span data-ttu-id="a7ac2-122">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-122">The deployment name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7ac2-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a7ac2-123">-InformationAction</span></span>
<span data-ttu-id="a7ac2-124">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a7ac2-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a7ac2-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a7ac2-126">Continuare</span><span class="sxs-lookup"><span data-stu-id="a7ac2-126">Continue</span></span>
- <span data-ttu-id="a7ac2-127">Ignora</span><span class="sxs-lookup"><span data-stu-id="a7ac2-127">Ignore</span></span>
- <span data-ttu-id="a7ac2-128">Informarsi</span><span class="sxs-lookup"><span data-stu-id="a7ac2-128">Inquire</span></span>
- <span data-ttu-id="a7ac2-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a7ac2-129">SilentlyContinue</span></span>
- <span data-ttu-id="a7ac2-130">Stop</span><span class="sxs-lookup"><span data-stu-id="a7ac2-130">Stop</span></span>
- <span data-ttu-id="a7ac2-131">Sospensione</span><span class="sxs-lookup"><span data-stu-id="a7ac2-131">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7ac2-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a7ac2-132">-InformationVariable</span></span>
<span data-ttu-id="a7ac2-133">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-133">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7ac2-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="a7ac2-134">-Pre</span></span>
<span data-ttu-id="a7ac2-135">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="a7ac2-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7ac2-136">-ResourceGroupName</span></span>
<span data-ttu-id="a7ac2-137">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-137">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7ac2-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a7ac2-138">-SubscriptionId</span></span>
<span data-ttu-id="a7ac2-139">La sottoscrizione da usare.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-139">The subscription to use.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7ac2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7ac2-140">CommonParameters</span></span>
<span data-ttu-id="a7ac2-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7ac2-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7ac2-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7ac2-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a7ac2-143">INPUTS</span></span>

### <span data-ttu-id="a7ac2-144">GUID</span><span class="sxs-lookup"><span data-stu-id="a7ac2-144">Guid</span></span>
<span data-ttu-id="a7ac2-145">Il parametro "SubscriptionId" accetta il valore di tipo "GUID" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="a7ac2-145">Parameter 'SubscriptionId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="a7ac2-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a7ac2-146">OUTPUTS</span></span>

### <span data-ttu-id="a7ac2-147">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a7ac2-147">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a7ac2-148">Note</span><span class="sxs-lookup"><span data-stu-id="a7ac2-148">NOTES</span></span>

## <span data-ttu-id="a7ac2-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a7ac2-149">RELATED LINKS</span></span>

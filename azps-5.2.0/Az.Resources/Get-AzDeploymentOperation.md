---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
ms.openlocfilehash: e1da6e54eac3e72217e83e498966bdfa80740762
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325368"
---
# <span data-ttu-id="9fc37-101">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="9fc37-101">Get-AzDeploymentOperation</span></span>

## <span data-ttu-id="9fc37-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9fc37-102">SYNOPSIS</span></span>
<span data-ttu-id="9fc37-103">Ottenere l'operazione di distribuzione</span><span class="sxs-lookup"><span data-stu-id="9fc37-103">Get deployment operation</span></span>

## <span data-ttu-id="9fc37-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9fc37-104">SYNTAX</span></span>

### <span data-ttu-id="9fc37-105">GetByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9fc37-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fc37-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="9fc37-106">GetByDeploymentObject</span></span>
```
Get-AzDeploymentOperation -DeploymentObject <PSDeployment> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9fc37-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9fc37-107">DESCRIPTION</span></span>
<span data-ttu-id="9fc37-108">Il cmdlet **Get-AzDeploymentOperation** elenca tutte le operazioni che facevano parte di una distribuzione per identificare e fornire ulteriori informazioni sulle operazioni esatte non riuscite per una specifica distribuzione.</span><span class="sxs-lookup"><span data-stu-id="9fc37-108">The **Get-AzDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="9fc37-109">Può anche visualizzare la risposta e il contenuto della richiesta per ogni operazione di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="9fc37-109">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="9fc37-110">Queste sono le stesse informazioni fornite nei dettagli di distribuzione nel portale.</span><span class="sxs-lookup"><span data-stu-id="9fc37-110">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="9fc37-111">Per ottenere la richiesta e il contenuto della risposta, abilitare l'impostazione quando si invia una distribuzione tramite **New-AzDeployment**.</span><span class="sxs-lookup"><span data-stu-id="9fc37-111">To get the request and the response content, enable the setting when submitting a deployment through **New-AzDeployment**.</span></span>
<span data-ttu-id="9fc37-112">Può potenzialmente registrare e esporre segreti come le password usate nella proprietà Resource o le operazioni di **listKeys** che vengono quindi restituite quando recuperi le operazioni di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="9fc37-112">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="9fc37-113">Per altre informazioni su questa impostazione e su come abilitarla, vedere New-AzDeployment e debug delle distribuzioni del modello ARM</span><span class="sxs-lookup"><span data-stu-id="9fc37-113">For more on this setting and how to enable it, see New-AzDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="9fc37-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9fc37-114">EXAMPLES</span></span>

### <span data-ttu-id="9fc37-115">Esempio 1: ottenere le operazioni di distribuzione in base a un nome di distribuzione</span><span class="sxs-lookup"><span data-stu-id="9fc37-115">Example 1: Get deployment operations given a deployment name</span></span>
```powershell
PS C:\>Get-AzDeploymentOperation -DeploymentName test
```

<span data-ttu-id="9fc37-116">Ottiene l'operazione di distribuzione con il nome "test" nell'ambito corrente della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="9fc37-116">Gets deployment operation with name "test" at the current subscription scope.</span></span>

### <span data-ttu-id="9fc37-117">Esempio 2: ottenere una distribuzione e ottenere le operazioni di distribuzione</span><span class="sxs-lookup"><span data-stu-id="9fc37-117">Example 2: Get a deployment and get its deployment operations</span></span>
```powershell
PS C:\>Get-AzDeployment -Name "test" | Get-AzDeploymentOperation
```

<span data-ttu-id="9fc37-118">Questo comando ottiene il "test" di distribuzione nell'ambito dell'abbonamento corrente e ottiene le operazioni di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="9fc37-118">This command gets the deployment "test" at the current subscription scope and get its deployment operations.</span></span>

## <span data-ttu-id="9fc37-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9fc37-119">PARAMETERS</span></span>

### <span data-ttu-id="9fc37-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fc37-120">-DefaultProfile</span></span>
<span data-ttu-id="9fc37-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9fc37-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fc37-122">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="9fc37-122">-DeploymentName</span></span>
<span data-ttu-id="9fc37-123">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="9fc37-123">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fc37-124">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="9fc37-124">-DeploymentObject</span></span>
<span data-ttu-id="9fc37-125">Oggetto Deployment.</span><span class="sxs-lookup"><span data-stu-id="9fc37-125">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fc37-126">-OperationId</span><span class="sxs-lookup"><span data-stu-id="9fc37-126">-OperationId</span></span>
<span data-ttu-id="9fc37-127">ID operazione di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="9fc37-127">The deployment operation Id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fc37-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="9fc37-128">-Pre</span></span>
<span data-ttu-id="9fc37-129">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="9fc37-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9fc37-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fc37-130">CommonParameters</span></span>
<span data-ttu-id="9fc37-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fc37-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fc37-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9fc37-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fc37-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9fc37-133">INPUTS</span></span>

### <span data-ttu-id="9fc37-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEPLOYMENT</span><span class="sxs-lookup"><span data-stu-id="9fc37-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="9fc37-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9fc37-135">OUTPUTS</span></span>

### <span data-ttu-id="9fc37-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="9fc37-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="9fc37-137">Note</span><span class="sxs-lookup"><span data-stu-id="9fc37-137">NOTES</span></span>

## <span data-ttu-id="9fc37-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9fc37-138">RELATED LINKS</span></span>

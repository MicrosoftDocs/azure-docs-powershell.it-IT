---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
ms.openlocfilehash: 5507e180d5f56b75006f31f9cc6753f50d821a3b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973613"
---
# <span data-ttu-id="c6a69-101">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="c6a69-101">Get-AzDeploymentOperation</span></span>

## <span data-ttu-id="c6a69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6a69-102">SYNOPSIS</span></span>
<span data-ttu-id="c6a69-103">Ottenere l'operazione di distribuzione</span><span class="sxs-lookup"><span data-stu-id="c6a69-103">Get deployment operation</span></span>

## <span data-ttu-id="c6a69-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c6a69-104">SYNTAX</span></span>

### <span data-ttu-id="c6a69-105">GetByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c6a69-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6a69-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="c6a69-106">GetByDeploymentObject</span></span>
```
Get-AzDeploymentOperation -DeploymentObject <PSDeployment> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6a69-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c6a69-107">DESCRIPTION</span></span>
<span data-ttu-id="c6a69-108">Il cmdlet **Get-AzDeploymentOperation** elenca tutte le operazioni che fanno parte di una distribuzione per consentire di identificare e fornire altre informazioni sulle esatte operazioni non riuscite per una particolare distribuzione.</span><span class="sxs-lookup"><span data-stu-id="c6a69-108">The **Get-AzDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="c6a69-109">Può anche mostrare la risposta e il contenuto della richiesta per ogni operazione di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="c6a69-109">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="c6a69-110">Si tratta delle stesse informazioni fornite nei dettagli della distribuzione nel portale.</span><span class="sxs-lookup"><span data-stu-id="c6a69-110">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="c6a69-111">Per ottenere la richiesta e il contenuto della risposta, abilitare l'impostazione quando si invia una distribuzione tramite **New-AzDeployment.**</span><span class="sxs-lookup"><span data-stu-id="c6a69-111">To get the request and the response content, enable the setting when submitting a deployment through **New-AzDeployment**.</span></span>
<span data-ttu-id="c6a69-112">Può potenzialmente registrare ed esporre segreti come le password usate nelle operazioni di proprietà delle risorse o **listKeys** che vengono quindi restituite quando si recuperano le operazioni di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="c6a69-112">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="c6a69-113">Per altre informazioni su questa impostazione e su come abilitarla, vedere New-AzDeployment distribuzione di modelli ARM debug</span><span class="sxs-lookup"><span data-stu-id="c6a69-113">For more on this setting and how to enable it, see New-AzDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="c6a69-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c6a69-114">EXAMPLES</span></span>

### <span data-ttu-id="c6a69-115">Esempio 1: Ottenere le operazioni di distribuzione con un nome di distribuzione</span><span class="sxs-lookup"><span data-stu-id="c6a69-115">Example 1: Get deployment operations given a deployment name</span></span>
```powershell
PS C:\>Get-AzDeploymentOperation -DeploymentName test
```

<span data-ttu-id="c6a69-116">Recupera l'operazione di distribuzione con il nome "test" nell'ambito della sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="c6a69-116">Gets deployment operation with name "test" at the current subscription scope.</span></span>

### <span data-ttu-id="c6a69-117">Esempio 2: Ottenere una distribuzione e ottenere le operazioni di distribuzione</span><span class="sxs-lookup"><span data-stu-id="c6a69-117">Example 2: Get a deployment and get its deployment operations</span></span>
```powershell
PS C:\>Get-AzDeployment -Name "test" | Get-AzDeploymentOperation
```

<span data-ttu-id="c6a69-118">Questo comando ottiene il "test" di distribuzione nell'ambito di sottoscrizione corrente e ottiene le operazioni di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="c6a69-118">This command gets the deployment "test" at the current subscription scope and get its deployment operations.</span></span>

## <span data-ttu-id="c6a69-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6a69-119">PARAMETERS</span></span>

### <span data-ttu-id="c6a69-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6a69-120">-DefaultProfile</span></span>
<span data-ttu-id="c6a69-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c6a69-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6a69-122">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="c6a69-122">-DeploymentName</span></span>
<span data-ttu-id="c6a69-123">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="c6a69-123">The deployment name.</span></span>

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

### <span data-ttu-id="c6a69-124">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="c6a69-124">-DeploymentObject</span></span>
<span data-ttu-id="c6a69-125">Oggetto di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="c6a69-125">The deployment object.</span></span>

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

### <span data-ttu-id="c6a69-126">-OperationId</span><span class="sxs-lookup"><span data-stu-id="c6a69-126">-OperationId</span></span>
<span data-ttu-id="c6a69-127">ID dell'operazione di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="c6a69-127">The deployment operation Id.</span></span>

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

### <span data-ttu-id="c6a69-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="c6a69-128">-Pre</span></span>
<span data-ttu-id="c6a69-129">Se impostato, indica che il cmdlet deve usare versioni delle API non beta per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="c6a69-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c6a69-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6a69-130">CommonParameters</span></span>
<span data-ttu-id="c6a69-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6a69-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6a69-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c6a69-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6a69-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="c6a69-133">INPUTS</span></span>

### <span data-ttu-id="c6a69-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="c6a69-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="c6a69-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c6a69-135">OUTPUTS</span></span>

### <span data-ttu-id="c6a69-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="c6a69-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="c6a69-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="c6a69-137">NOTES</span></span>

## <span data-ttu-id="c6a69-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c6a69-138">RELATED LINKS</span></span>

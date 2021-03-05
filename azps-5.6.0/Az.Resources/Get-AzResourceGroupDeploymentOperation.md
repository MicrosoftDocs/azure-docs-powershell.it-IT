---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresourcegroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
ms.openlocfilehash: 06056bd8bf9060a7610b74b8332ff5ab2a4790f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973533"
---
# <span data-ttu-id="9f15c-101">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="9f15c-101">Get-AzResourceGroupDeploymentOperation</span></span>

## <span data-ttu-id="9f15c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f15c-102">SYNOPSIS</span></span>
<span data-ttu-id="9f15c-103">Recupera l'operazione di distribuzione del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="9f15c-103">Gets the resource group deployment operation</span></span>

## <span data-ttu-id="9f15c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9f15c-104">SYNTAX</span></span>

```
Get-AzResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f15c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9f15c-105">DESCRIPTION</span></span>
<span data-ttu-id="9f15c-106">Il cmdlet **Get-AzResourceGroupDeploymentOperation** elenca tutte le operazioni che fanno parte di una distribuzione per consentire di identificare e fornire altre informazioni sulle esatte operazioni non riuscite per una particolare distribuzione.</span><span class="sxs-lookup"><span data-stu-id="9f15c-106">The **Get-AzResourceGroupDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="9f15c-107">Può anche mostrare la risposta e il contenuto della richiesta per ogni operazione di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="9f15c-107">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="9f15c-108">Si tratta delle stesse informazioni fornite nei dettagli della distribuzione nel portale.</span><span class="sxs-lookup"><span data-stu-id="9f15c-108">This is the same information provided in the deployment details on the portal.</span></span>
<span data-ttu-id="9f15c-109">Per ottenere la richiesta e il contenuto della risposta, abilitare l'impostazione quando si invia una distribuzione tramite **New-AzResourceGroupDeployment.**</span><span class="sxs-lookup"><span data-stu-id="9f15c-109">To get the request and the response content, enable the setting when submitting a deployment through **New-AzResourceGroupDeployment**.</span></span>
<span data-ttu-id="9f15c-110">Può potenzialmente registrare ed esporre segreti come le password usate nelle operazioni di proprietà delle risorse o **listKeys** che vengono quindi restituite quando si recuperano le operazioni di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="9f15c-110">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="9f15c-111">Per altre informazioni su questa impostazione e su come abilitarla, vedere New-AzResourceGroupDeployment distribuzione di modelli ARM debug</span><span class="sxs-lookup"><span data-stu-id="9f15c-111">For more on this setting and how to enable it, see New-AzResourceGroupDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="9f15c-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9f15c-112">EXAMPLES</span></span>

### <span data-ttu-id="9f15c-113">Esempio 1: Get1</span><span class="sxs-lookup"><span data-stu-id="9f15c-113">Example 1: Get1</span></span>
```powershell
PS C:\>Get-AzResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

<span data-ttu-id="9f15c-114">Recupera l'operazione di distribuzione con il nome "test" nel gruppo di risorse "test"</span><span class="sxs-lookup"><span data-stu-id="9f15c-114">Gets deployment operation with name "test" under resource group "test"</span></span>

## <span data-ttu-id="9f15c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f15c-115">PARAMETERS</span></span>

### <span data-ttu-id="9f15c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f15c-116">-DefaultProfile</span></span>
<span data-ttu-id="9f15c-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9f15c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f15c-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="9f15c-118">-DeploymentName</span></span>
<span data-ttu-id="9f15c-119">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="9f15c-119">The deployment name.</span></span>

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

### <span data-ttu-id="9f15c-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="9f15c-120">-Pre</span></span>
<span data-ttu-id="9f15c-121">Se impostato, indica che il cmdlet deve usare versioni delle API non definitiva per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="9f15c-121">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9f15c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f15c-122">-ResourceGroupName</span></span>
<span data-ttu-id="9f15c-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9f15c-123">The resource group name.</span></span>

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

### <span data-ttu-id="9f15c-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9f15c-124">-SubscriptionId</span></span>
<span data-ttu-id="9f15c-125">L'abbonamento da usare.</span><span class="sxs-lookup"><span data-stu-id="9f15c-125">The subscription to use.</span></span>

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

### <span data-ttu-id="9f15c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f15c-126">CommonParameters</span></span>
<span data-ttu-id="9f15c-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f15c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f15c-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9f15c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f15c-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="9f15c-129">INPUTS</span></span>

### <span data-ttu-id="9f15c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="9f15c-130">System.String</span></span>

### <span data-ttu-id="9f15c-131">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9f15c-131">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9f15c-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9f15c-132">OUTPUTS</span></span>

### <span data-ttu-id="9f15c-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="9f15c-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="9f15c-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="9f15c-134">NOTES</span></span>

## <span data-ttu-id="9f15c-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9f15c-135">RELATED LINKS</span></span>

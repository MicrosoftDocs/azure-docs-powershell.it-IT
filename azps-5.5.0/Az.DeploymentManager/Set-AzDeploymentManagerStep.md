---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
ms.openlocfilehash: 2cd73cad57f36130ed11e37ad6dc2147e6c081ae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209754"
---
# <span data-ttu-id="d0b50-101">Set-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="d0b50-101">Set-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="d0b50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0b50-102">SYNOPSIS</span></span>
<span data-ttu-id="d0b50-103">Aggiorna il passaggio.</span><span class="sxs-lookup"><span data-stu-id="d0b50-103">Updates the step.</span></span>

## <span data-ttu-id="d0b50-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d0b50-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0b50-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d0b50-105">DESCRIPTION</span></span>
<span data-ttu-id="d0b50-106">Il **cmdlet Set-AzDeploymentManagerStep** aggiorna un passaggio con l'oggetto passaggio specificato.</span><span class="sxs-lookup"><span data-stu-id="d0b50-106">The **Set-AzDeploymentManagerStep** cmdlet updates a step with the specified step object.</span></span>
<span data-ttu-id="d0b50-107">Il cmdlet restituisce l'oggetto passaggio aggiornato.</span><span class="sxs-lookup"><span data-stu-id="d0b50-107">The cmdlet returns the updated step object.</span></span>

## <span data-ttu-id="d0b50-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d0b50-108">EXAMPLES</span></span>

### <span data-ttu-id="d0b50-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d0b50-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerStep -InputObject $stepObject
```

<span data-ttu-id="d0b50-110">Questo comando aggiorna un passaggio il cui nome e GruppoSocietà Risorse corrispondono rispettivamente alle proprietà Name e ResourceGroupName dell'$stepObject risorsa.</span><span class="sxs-lookup"><span data-stu-id="d0b50-110">This command updates a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>
<span data-ttu-id="d0b50-111">Il passaggio verrà aggiornato alle proprietà impostate nel $stepObject.</span><span class="sxs-lookup"><span data-stu-id="d0b50-111">The step would be updated to the properties set in the $stepObject.</span></span>

## <span data-ttu-id="d0b50-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0b50-112">PARAMETERS</span></span>

### <span data-ttu-id="d0b50-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0b50-113">-DefaultProfile</span></span>
<span data-ttu-id="d0b50-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d0b50-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0b50-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0b50-115">-InputObject</span></span>
<span data-ttu-id="d0b50-116">Oggetto di passaggio.</span><span class="sxs-lookup"><span data-stu-id="d0b50-116">The step object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0b50-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0b50-117">-Confirm</span></span>
<span data-ttu-id="d0b50-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0b50-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0b50-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0b50-119">-WhatIf</span></span>
<span data-ttu-id="d0b50-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0b50-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0b50-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0b50-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0b50-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0b50-122">CommonParameters</span></span>
<span data-ttu-id="d0b50-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0b50-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0b50-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d0b50-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0b50-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="d0b50-125">INPUTS</span></span>

### <span data-ttu-id="d0b50-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="d0b50-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="d0b50-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d0b50-127">OUTPUTS</span></span>

### <span data-ttu-id="d0b50-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="d0b50-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="d0b50-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="d0b50-129">NOTES</span></span>

## <span data-ttu-id="d0b50-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d0b50-130">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
ms.openlocfilehash: 2cd73cad57f36130ed11e37ad6dc2147e6c081ae
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190763"
---
# <span data-ttu-id="373d6-101">Set-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="373d6-101">Set-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="373d6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="373d6-102">SYNOPSIS</span></span>
<span data-ttu-id="373d6-103">Aggiorna il passaggio.</span><span class="sxs-lookup"><span data-stu-id="373d6-103">Updates the step.</span></span>

## <span data-ttu-id="373d6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="373d6-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="373d6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="373d6-105">DESCRIPTION</span></span>
<span data-ttu-id="373d6-106">Il cmdlet **set-AzDeploymentManagerStep** aggiorna un passaggio con l'oggetto Step specificato.</span><span class="sxs-lookup"><span data-stu-id="373d6-106">The **Set-AzDeploymentManagerStep** cmdlet updates a step with the specified step object.</span></span>
<span data-ttu-id="373d6-107">Il cmdlet restituisce l'oggetto passaggio aggiornato.</span><span class="sxs-lookup"><span data-stu-id="373d6-107">The cmdlet returns the updated step object.</span></span>

## <span data-ttu-id="373d6-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="373d6-108">EXAMPLES</span></span>

### <span data-ttu-id="373d6-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="373d6-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerStep -InputObject $stepObject
```

<span data-ttu-id="373d6-110">Questo comando aggiorna un passaggio il cui nome e ResourceGroup corrispondono rispettivamente alle proprietà Name e ResourceGroupName della $stepObject.</span><span class="sxs-lookup"><span data-stu-id="373d6-110">This command updates a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>
<span data-ttu-id="373d6-111">Il passaggio verrà aggiornato alle proprietà impostate nel $stepObject.</span><span class="sxs-lookup"><span data-stu-id="373d6-111">The step would be updated to the properties set in the $stepObject.</span></span>

## <span data-ttu-id="373d6-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="373d6-112">PARAMETERS</span></span>

### <span data-ttu-id="373d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="373d6-113">-DefaultProfile</span></span>
<span data-ttu-id="373d6-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="373d6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="373d6-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="373d6-115">-InputObject</span></span>
<span data-ttu-id="373d6-116">Oggetto Step.</span><span class="sxs-lookup"><span data-stu-id="373d6-116">The step object.</span></span>

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

### <span data-ttu-id="373d6-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="373d6-117">-Confirm</span></span>
<span data-ttu-id="373d6-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="373d6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="373d6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="373d6-119">-WhatIf</span></span>
<span data-ttu-id="373d6-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="373d6-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="373d6-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="373d6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="373d6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="373d6-122">CommonParameters</span></span>
<span data-ttu-id="373d6-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="373d6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="373d6-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="373d6-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="373d6-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="373d6-125">INPUTS</span></span>

### <span data-ttu-id="373d6-126">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="373d6-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="373d6-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="373d6-127">OUTPUTS</span></span>

### <span data-ttu-id="373d6-128">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="373d6-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="373d6-129">Note</span><span class="sxs-lookup"><span data-stu-id="373d6-129">NOTES</span></span>

## <span data-ttu-id="373d6-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="373d6-130">RELATED LINKS</span></span>
---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: 7241e072109583b7afc24fc3f69746599bd67c53
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491277"
---
# <span data-ttu-id="dc129-101">Set-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="dc129-101">Set-AzureRmDeploymentManagerStep</span></span>

## <span data-ttu-id="dc129-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dc129-102">SYNOPSIS</span></span>
<span data-ttu-id="dc129-103">Aggiorna un passaggio.</span><span class="sxs-lookup"><span data-stu-id="dc129-103">Updates a step.</span></span>

## <span data-ttu-id="dc129-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dc129-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerStep [-Step] <PSStepResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc129-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dc129-105">DESCRIPTION</span></span>
<span data-ttu-id="dc129-106">Il cmdlet **set-AzureRmDeploymentManagerStep** aggiorna un passaggio con l'oggetto Step specificato.</span><span class="sxs-lookup"><span data-stu-id="dc129-106">The **Set-AzureRmDeploymentManagerStep** cmdlet updates a step with the specified step object.</span></span>
<span data-ttu-id="dc129-107">Il cmdlet restituisce l'oggetto passaggio aggiornato.</span><span class="sxs-lookup"><span data-stu-id="dc129-107">The cmdlet returns the updated step object.</span></span>

## <span data-ttu-id="dc129-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dc129-108">EXAMPLES</span></span>

### <span data-ttu-id="dc129-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dc129-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmDeploymentManagerStep -Step $stepObject
```

<span data-ttu-id="dc129-110">Questo comando aggiorna un passaggio il cui nome e ResourceGroup corrispondono rispettivamente alle proprietà Name e ResourceGroupName della $stepObject.</span><span class="sxs-lookup"><span data-stu-id="dc129-110">This command updates a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>
<span data-ttu-id="dc129-111">Il passaggio verrà aggiornato alle proprietà impostate nel $stepObject.</span><span class="sxs-lookup"><span data-stu-id="dc129-111">The step would be updated to the properties set in the $stepObject.</span></span>

## <span data-ttu-id="dc129-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dc129-112">PARAMETERS</span></span>

### <span data-ttu-id="dc129-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc129-113">-DefaultProfile</span></span>
<span data-ttu-id="dc129-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dc129-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc129-115">-Step</span><span class="sxs-lookup"><span data-stu-id="dc129-115">-Step</span></span>
<span data-ttu-id="dc129-116">Oggetto Step.</span><span class="sxs-lookup"><span data-stu-id="dc129-116">The step object.</span></span>

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

### <span data-ttu-id="dc129-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dc129-117">-Confirm</span></span>
<span data-ttu-id="dc129-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc129-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc129-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc129-119">-WhatIf</span></span>
<span data-ttu-id="dc129-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dc129-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc129-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dc129-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc129-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc129-122">CommonParameters</span></span>
<span data-ttu-id="dc129-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc129-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="dc129-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc129-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc129-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dc129-125">INPUTS</span></span>

### <span data-ttu-id="dc129-126">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="dc129-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="dc129-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dc129-127">OUTPUTS</span></span>

### <span data-ttu-id="dc129-128">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="dc129-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="dc129-129">Note</span><span class="sxs-lookup"><span data-stu-id="dc129-129">NOTES</span></span>

## <span data-ttu-id="dc129-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dc129-130">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/uninstall-azurerm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
ms.openlocfilehash: 796690bd0a5774e488b978003c48b02eedaac190
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967086"
---
# <span data-ttu-id="906eb-101">Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="906eb-101">Uninstall-AzureRm</span></span>

## <span data-ttu-id="906eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="906eb-102">SYNOPSIS</span></span>
<span data-ttu-id="906eb-103">Rimuove tutti i moduli di AzureRm da un computer.</span><span class="sxs-lookup"><span data-stu-id="906eb-103">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="906eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="906eb-104">SYNTAX</span></span>

```
Uninstall-AzureRm [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="906eb-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="906eb-105">DESCRIPTION</span></span>
<span data-ttu-id="906eb-106">Rimuove tutti i moduli di AzureRm da un computer.</span><span class="sxs-lookup"><span data-stu-id="906eb-106">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="906eb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="906eb-107">EXAMPLES</span></span>

### <span data-ttu-id="906eb-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="906eb-108">Example 1</span></span>
```
PS C:\> Uninstall-AzureRm
```

<span data-ttu-id="906eb-109">L'esecuzione di questo comando rimuove tutti i moduli di AzureRm dal computer per la versione di PowerShell in cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="906eb-109">Running this command will remove all AzureRm modules from the machine for the version of PowerShell in which the cmdlet is run.</span></span>

## <span data-ttu-id="906eb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="906eb-110">PARAMETERS</span></span>

### <span data-ttu-id="906eb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="906eb-111">-DefaultProfile</span></span>
<span data-ttu-id="906eb-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="906eb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="906eb-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="906eb-113">-PassThru</span></span>
<span data-ttu-id="906eb-114">Restituisce l'elenco dei moduli rimossi, se specificato.</span><span class="sxs-lookup"><span data-stu-id="906eb-114">Return list of Modules removed if specified.</span></span>

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

### <span data-ttu-id="906eb-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="906eb-115">-Confirm</span></span>
<span data-ttu-id="906eb-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="906eb-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="906eb-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="906eb-117">-WhatIf</span></span>
<span data-ttu-id="906eb-118">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="906eb-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="906eb-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="906eb-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="906eb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="906eb-120">CommonParameters</span></span>
<span data-ttu-id="906eb-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="906eb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="906eb-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="906eb-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="906eb-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="906eb-123">INPUTS</span></span>

### <span data-ttu-id="906eb-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="906eb-124">None</span></span>

## <span data-ttu-id="906eb-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="906eb-125">OUTPUTS</span></span>

### <span data-ttu-id="906eb-126">System.String</span><span class="sxs-lookup"><span data-stu-id="906eb-126">System.String</span></span>

## <span data-ttu-id="906eb-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="906eb-127">NOTES</span></span>

## <span data-ttu-id="906eb-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="906eb-128">RELATED LINKS</span></span>

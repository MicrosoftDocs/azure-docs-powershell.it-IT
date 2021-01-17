---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/uninstall-azurerm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
ms.openlocfilehash: ee581528810663d09fe724f370b681ff9e20072f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475994"
---
# <span data-ttu-id="8cfc0-101">Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="8cfc0-101">Uninstall-AzureRm</span></span>

## <span data-ttu-id="8cfc0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8cfc0-102">SYNOPSIS</span></span>
<span data-ttu-id="8cfc0-103">Rimuove tutti i moduli AzureRm da un computer.</span><span class="sxs-lookup"><span data-stu-id="8cfc0-103">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="8cfc0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8cfc0-104">SYNTAX</span></span>

```
Uninstall-AzureRm [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8cfc0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8cfc0-105">DESCRIPTION</span></span>
<span data-ttu-id="8cfc0-106">Rimuove tutti i moduli AzureRm da un computer.</span><span class="sxs-lookup"><span data-stu-id="8cfc0-106">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="8cfc0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8cfc0-107">EXAMPLES</span></span>

### <span data-ttu-id="8cfc0-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8cfc0-108">Example 1</span></span>
```
PS C:\> Uninstall-AzureRm
```

<span data-ttu-id="8cfc0-109">L'esecuzione di questo comando consente di rimuovere tutti i moduli AzureRm dal computer per la versione di PowerShell in cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cfc0-109">Running this command will remove all AzureRm modules from the machine for the version of PowerShell in which the cmdlet is run.</span></span>

## <span data-ttu-id="8cfc0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8cfc0-110">PARAMETERS</span></span>

### <span data-ttu-id="8cfc0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cfc0-111">-DefaultProfile</span></span>
<span data-ttu-id="8cfc0-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8cfc0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cfc0-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8cfc0-113">-PassThru</span></span>
<span data-ttu-id="8cfc0-114">Restituisce l'elenco dei moduli rimossi se specificato.</span><span class="sxs-lookup"><span data-stu-id="8cfc0-114">Return list of Modules removed if specified.</span></span>

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

### <span data-ttu-id="8cfc0-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8cfc0-115">-Confirm</span></span>
<span data-ttu-id="8cfc0-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cfc0-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cfc0-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cfc0-117">-WhatIf</span></span>
<span data-ttu-id="8cfc0-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8cfc0-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cfc0-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8cfc0-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cfc0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cfc0-120">CommonParameters</span></span>
<span data-ttu-id="8cfc0-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cfc0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cfc0-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cfc0-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cfc0-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8cfc0-123">INPUTS</span></span>

### <span data-ttu-id="8cfc0-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8cfc0-124">None</span></span>

## <span data-ttu-id="8cfc0-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8cfc0-125">OUTPUTS</span></span>

### <span data-ttu-id="8cfc0-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8cfc0-126">System.String</span></span>

## <span data-ttu-id="8cfc0-127">Note</span><span class="sxs-lookup"><span data-stu-id="8cfc0-127">NOTES</span></span>

## <span data-ttu-id="8cfc0-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8cfc0-128">RELATED LINKS</span></span>

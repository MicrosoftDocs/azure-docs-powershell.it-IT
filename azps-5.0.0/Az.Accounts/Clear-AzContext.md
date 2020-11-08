---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
ms.openlocfilehash: b808f9272c000ed0ef17079dd31800860a31449b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199765"
---
# <span data-ttu-id="0cb00-101">Clear-AzContext</span><span class="sxs-lookup"><span data-stu-id="0cb00-101">Clear-AzContext</span></span>

## <span data-ttu-id="0cb00-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0cb00-102">SYNOPSIS</span></span>
<span data-ttu-id="0cb00-103">Rimuovere tutte le informazioni sulle credenziali, l'account e l'abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="0cb00-103">Remove all Azure credentials, account, and subscription information.</span></span>

## <span data-ttu-id="0cb00-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0cb00-104">SYNTAX</span></span>

```
Clear-AzContext [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cb00-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0cb00-105">DESCRIPTION</span></span>
<span data-ttu-id="0cb00-106">Rimuovere tutte le informazioni sulle credenziali, l'account e l'abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="0cb00-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="0cb00-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0cb00-107">EXAMPLES</span></span>

### <span data-ttu-id="0cb00-108">Esempio 1: cancellare il contesto globale</span><span class="sxs-lookup"><span data-stu-id="0cb00-108">Example 1: Clear global context</span></span>
```powershell
PS C:\> Clear-AzContext -Scope CurrentUser
```

<span data-ttu-id="0cb00-109">Rimuovere tutte le informazioni sull'account, l'abbonamento e le credenziali per qualsiasi sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0cb00-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="0cb00-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0cb00-110">PARAMETERS</span></span>

### <span data-ttu-id="0cb00-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cb00-111">-DefaultProfile</span></span>
<span data-ttu-id="0cb00-112">Credenziali, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0cb00-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0cb00-113">-Force</span><span class="sxs-lookup"><span data-stu-id="0cb00-113">-Force</span></span>
<span data-ttu-id="0cb00-114">Eliminare tutti gli utenti e i gruppi dall'ambito globale senza richiedere conferma</span><span class="sxs-lookup"><span data-stu-id="0cb00-114">Delete all users and groups from the global scope without prompting</span></span>

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

### <span data-ttu-id="0cb00-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0cb00-115">-PassThru</span></span>
<span data-ttu-id="0cb00-116">Restituire un valore che indica l'esito positivo o negativo</span><span class="sxs-lookup"><span data-stu-id="0cb00-116">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="0cb00-117">-Ambito</span><span class="sxs-lookup"><span data-stu-id="0cb00-117">-Scope</span></span>
<span data-ttu-id="0cb00-118">Deselezionare il contesto solo per la sessione di PowerShell corrente o per tutte le sessioni.</span><span class="sxs-lookup"><span data-stu-id="0cb00-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cb00-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0cb00-119">-Confirm</span></span>
<span data-ttu-id="0cb00-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cb00-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cb00-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cb00-121">-WhatIf</span></span>
<span data-ttu-id="0cb00-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0cb00-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cb00-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0cb00-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cb00-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cb00-124">CommonParameters</span></span>
<span data-ttu-id="0cb00-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cb00-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cb00-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cb00-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cb00-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0cb00-127">INPUTS</span></span>

### <span data-ttu-id="0cb00-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0cb00-128">None</span></span>

## <span data-ttu-id="0cb00-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0cb00-129">OUTPUTS</span></span>

### <span data-ttu-id="0cb00-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0cb00-130">System.Boolean</span></span>

## <span data-ttu-id="0cb00-131">Note</span><span class="sxs-lookup"><span data-stu-id="0cb00-131">NOTES</span></span>

## <span data-ttu-id="0cb00-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0cb00-132">RELATED LINKS</span></span>

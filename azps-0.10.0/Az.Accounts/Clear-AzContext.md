---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Clear-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Clear-AzContext.md
ms.openlocfilehash: 9dcf7b7d7149235d5a2ed211dbccf87415f1c496
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860094"
---
# <span data-ttu-id="c15c8-101">Clear-AzContext</span><span class="sxs-lookup"><span data-stu-id="c15c8-101">Clear-AzContext</span></span>

## <span data-ttu-id="c15c8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c15c8-102">SYNOPSIS</span></span>
<span data-ttu-id="c15c8-103">Rimuovere tutte le informazioni sulle credenziali, l'account e l'abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="c15c8-103">Remove all Azure credentials, account, and subscription information.</span></span>

## <span data-ttu-id="c15c8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c15c8-104">SYNTAX</span></span>

```
Clear-AzContext [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c15c8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c15c8-105">DESCRIPTION</span></span>
<span data-ttu-id="c15c8-106">Rimuovere tutte le informazioni sulle credenziali, l'account e l'abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="c15c8-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="c15c8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c15c8-107">EXAMPLES</span></span>

### <span data-ttu-id="c15c8-108">Cancellare un contesto globale</span><span class="sxs-lookup"><span data-stu-id="c15c8-108">Clear global context</span></span>
```
PS C:\> Clear-AzContext -Scope CurrentUser
```

<span data-ttu-id="c15c8-109">Rimuovere tutte le informazioni sull'account, l'abbonamento e le credenziali per qualsiasi sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c15c8-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="c15c8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c15c8-110">PARAMETERS</span></span>

### <span data-ttu-id="c15c8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c15c8-111">-DefaultProfile</span></span>
<span data-ttu-id="c15c8-112">Credenziali, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c15c8-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c15c8-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c15c8-113">-Force</span></span>
<span data-ttu-id="c15c8-114">Eliminare tutti gli utenti e i gruppi dall'ambito globale senza richiedere conferma</span><span class="sxs-lookup"><span data-stu-id="c15c8-114">Delete all users and groups from the global scope without prompting</span></span>

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

### <span data-ttu-id="c15c8-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c15c8-115">-PassThru</span></span>
<span data-ttu-id="c15c8-116">Restituire un valore che indica l'esito positivo o negativo</span><span class="sxs-lookup"><span data-stu-id="c15c8-116">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="c15c8-117">-Ambito</span><span class="sxs-lookup"><span data-stu-id="c15c8-117">-Scope</span></span>
<span data-ttu-id="c15c8-118">Deselezionare il contesto solo per la sessione di PowerShell corrente o per tutte le sessioni.</span><span class="sxs-lookup"><span data-stu-id="c15c8-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

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

### <span data-ttu-id="c15c8-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c15c8-119">-Confirm</span></span>
<span data-ttu-id="c15c8-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c15c8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c15c8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c15c8-121">-WhatIf</span></span>
<span data-ttu-id="c15c8-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c15c8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c15c8-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c15c8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c15c8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c15c8-124">CommonParameters</span></span>
<span data-ttu-id="c15c8-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c15c8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c15c8-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c15c8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c15c8-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c15c8-127">INPUTS</span></span>

### <span data-ttu-id="c15c8-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c15c8-128">None</span></span>

## <span data-ttu-id="c15c8-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c15c8-129">OUTPUTS</span></span>

### <span data-ttu-id="c15c8-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c15c8-130">System.Boolean</span></span>

## <span data-ttu-id="c15c8-131">Note</span><span class="sxs-lookup"><span data-stu-id="c15c8-131">NOTES</span></span>

## <span data-ttu-id="c15c8-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c15c8-132">RELATED LINKS</span></span>

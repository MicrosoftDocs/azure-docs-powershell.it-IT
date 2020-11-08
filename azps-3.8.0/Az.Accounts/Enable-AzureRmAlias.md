---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
ms.openlocfilehash: 63873d3eb1c46b5c2a4004e9c361f87e74e73eba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020981"
---
# <span data-ttu-id="bb1b8-101">Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="bb1b8-101">Enable-AzureRmAlias</span></span>

## <span data-ttu-id="bb1b8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bb1b8-102">SYNOPSIS</span></span>
<span data-ttu-id="bb1b8-103">Abilita gli alias di prefisso AzureRm per i moduli AZ.</span><span class="sxs-lookup"><span data-stu-id="bb1b8-103">Enables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="bb1b8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb1b8-104">SYNTAX</span></span>

```
Enable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb1b8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb1b8-105">DESCRIPTION</span></span>
<span data-ttu-id="bb1b8-106">Abilita gli alias di prefisso AzureRm per i moduli AZ.</span><span class="sxs-lookup"><span data-stu-id="bb1b8-106">Enables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="bb1b8-107">Se-Module è specificato, solo i moduli elencati avranno gli alias abilitati.</span><span class="sxs-lookup"><span data-stu-id="bb1b8-107">If -Module is specified, only modules listed will have aliases enabled.</span></span> <span data-ttu-id="bb1b8-108">In caso contrario, tutti gli alias di AzureRm sono abilitati.</span><span class="sxs-lookup"><span data-stu-id="bb1b8-108">Otherwise all AzureRm aliases are enabled.</span></span>

## <span data-ttu-id="bb1b8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb1b8-109">EXAMPLES</span></span>

### <span data-ttu-id="bb1b8-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bb1b8-110">Example 1</span></span>
```
PS C:\> Enable-AzureRmAlias
```

<span data-ttu-id="bb1b8-111">Abilita tutti i prefissi di AzureRm per la sessione corrente di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bb1b8-111">Enables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="bb1b8-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bb1b8-112">Example 1</span></span>
```
PS C:\> Enable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="bb1b8-113">Abilita gli alias di AzureRm per il modulo AZ. Accounts sia per il processo corrente che per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="bb1b8-113">Enables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="bb1b8-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bb1b8-114">PARAMETERS</span></span>

### <span data-ttu-id="bb1b8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb1b8-115">-DefaultProfile</span></span>
<span data-ttu-id="bb1b8-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bb1b8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb1b8-117">-Module</span><span class="sxs-lookup"><span data-stu-id="bb1b8-117">-Module</span></span>
<span data-ttu-id="bb1b8-118">Indica i moduli per cui abilitare gli alias.</span><span class="sxs-lookup"><span data-stu-id="bb1b8-118">Indicates which modules to enable aliases for.</span></span>
<span data-ttu-id="bb1b8-119">Se non si specifica nessuno, il valore predefinito è tutti i moduli.</span><span class="sxs-lookup"><span data-stu-id="bb1b8-119">If none are specified, default is all modules.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb1b8-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb1b8-120">-PassThru</span></span>
<span data-ttu-id="bb1b8-121">Se specificato, cmdlet restituirà tutti gli alias abilitati</span><span class="sxs-lookup"><span data-stu-id="bb1b8-121">If specified, cmdlet will return all aliases enabled</span></span>

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

### <span data-ttu-id="bb1b8-122">-Ambito</span><span class="sxs-lookup"><span data-stu-id="bb1b8-122">-Scope</span></span>
<span data-ttu-id="bb1b8-123">Indica quali alias di ambito devono essere abilitati.</span><span class="sxs-lookup"><span data-stu-id="bb1b8-123">Indicates what scope aliases should be enabled for.</span></span> <span data-ttu-id="bb1b8-124">Il valore predefinito è "local"</span><span class="sxs-lookup"><span data-stu-id="bb1b8-124">Default is 'Local'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Process, CurrentUser, LocalMachine

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb1b8-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bb1b8-125">-Confirm</span></span>
<span data-ttu-id="bb1b8-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb1b8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb1b8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb1b8-127">-WhatIf</span></span>
<span data-ttu-id="bb1b8-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb1b8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb1b8-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb1b8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb1b8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb1b8-130">CommonParameters</span></span>
<span data-ttu-id="bb1b8-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb1b8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb1b8-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb1b8-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb1b8-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bb1b8-133">INPUTS</span></span>

### <span data-ttu-id="bb1b8-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bb1b8-134">None</span></span>

## <span data-ttu-id="bb1b8-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb1b8-135">OUTPUTS</span></span>

### <span data-ttu-id="bb1b8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="bb1b8-136">System.String</span></span>

## <span data-ttu-id="bb1b8-137">Note</span><span class="sxs-lookup"><span data-stu-id="bb1b8-137">NOTES</span></span>

## <span data-ttu-id="bb1b8-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb1b8-138">RELATED LINKS</span></span>

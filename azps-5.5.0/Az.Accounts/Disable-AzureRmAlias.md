---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
ms.openlocfilehash: 749507ba0bc0eec8aac7600c5262533ceb02a46b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178142"
---
# <span data-ttu-id="c283e-101">Disable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="c283e-101">Disable-AzureRmAlias</span></span>

## <span data-ttu-id="c283e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c283e-102">SYNOPSIS</span></span>
<span data-ttu-id="c283e-103">Disabilita gli alias dei prefissi AzureRm per i moduli Az.</span><span class="sxs-lookup"><span data-stu-id="c283e-103">Disables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="c283e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c283e-104">SYNTAX</span></span>

```
Disable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c283e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c283e-105">DESCRIPTION</span></span>
<span data-ttu-id="c283e-106">Disabilita gli alias dei prefissi AzureRm per i moduli Az.</span><span class="sxs-lookup"><span data-stu-id="c283e-106">Disables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="c283e-107">Se si specificato -Module, solo i moduli elencati avranno gli alias disabilitati.</span><span class="sxs-lookup"><span data-stu-id="c283e-107">If -Module is specified, only modules listed will have aliases disabled.</span></span> <span data-ttu-id="c283e-108">In caso contrario, tutti gli alias di AzureRm verranno disabilitati.</span><span class="sxs-lookup"><span data-stu-id="c283e-108">Otherwise all AzureRm aliases are disabled.</span></span>

## <span data-ttu-id="c283e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c283e-109">EXAMPLES</span></span>

### <span data-ttu-id="c283e-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c283e-110">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias
```

<span data-ttu-id="c283e-111">Disabilita tutti i prefissi AzureRm per la sessione di PowerShell corrente.</span><span class="sxs-lookup"><span data-stu-id="c283e-111">Disables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="c283e-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c283e-112">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="c283e-113">Disabilita gli alias di AzureRm per il modulo Az.Accounts sia per il processo corrente che per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="c283e-113">Disables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="c283e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c283e-114">PARAMETERS</span></span>

### <span data-ttu-id="c283e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c283e-115">-DefaultProfile</span></span>
<span data-ttu-id="c283e-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c283e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c283e-117">-Module</span><span class="sxs-lookup"><span data-stu-id="c283e-117">-Module</span></span>
<span data-ttu-id="c283e-118">Indica per quali moduli disabilitare gli alias.</span><span class="sxs-lookup"><span data-stu-id="c283e-118">Indicates which modules to disable aliases for.</span></span>
<span data-ttu-id="c283e-119">Se non ne viene specificato nessuno, il valore predefinito è tutti i moduli abilitati.</span><span class="sxs-lookup"><span data-stu-id="c283e-119">If none are specified, default is all enabled modules.</span></span>

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

### <span data-ttu-id="c283e-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c283e-120">-PassThru</span></span>
<span data-ttu-id="c283e-121">Se specificato, il cmdlet restituirà tutti gli alias disabilitati</span><span class="sxs-lookup"><span data-stu-id="c283e-121">If specified, cmdlet will return all disabled aliases</span></span>

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

### <span data-ttu-id="c283e-122">-Scope</span><span class="sxs-lookup"><span data-stu-id="c283e-122">-Scope</span></span>
<span data-ttu-id="c283e-123">Indica per quali alias di ambito devono essere disabilitati.</span><span class="sxs-lookup"><span data-stu-id="c283e-123">Indicates what scope aliases should be disabled for.</span></span> <span data-ttu-id="c283e-124">L'impostazione predefinita è "Processo"</span><span class="sxs-lookup"><span data-stu-id="c283e-124">Default is 'Process'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser, LocalMachine

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c283e-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c283e-125">-Confirm</span></span>
<span data-ttu-id="c283e-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c283e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c283e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c283e-127">-WhatIf</span></span>
<span data-ttu-id="c283e-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c283e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c283e-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c283e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c283e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c283e-130">CommonParameters</span></span>
<span data-ttu-id="c283e-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c283e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c283e-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c283e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c283e-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="c283e-133">INPUTS</span></span>

### <span data-ttu-id="c283e-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c283e-134">None</span></span>

## <span data-ttu-id="c283e-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c283e-135">OUTPUTS</span></span>

### <span data-ttu-id="c283e-136">System.String</span><span class="sxs-lookup"><span data-stu-id="c283e-136">System.String</span></span>

## <span data-ttu-id="c283e-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="c283e-137">NOTES</span></span>

## <span data-ttu-id="c283e-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c283e-138">RELATED LINKS</span></span>

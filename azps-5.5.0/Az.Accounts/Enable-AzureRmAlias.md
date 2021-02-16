---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
ms.openlocfilehash: 6a530a0e20f3e69540320ad3eab8b8cc7f37b5af
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195431"
---
# <span data-ttu-id="7adb7-101">Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="7adb7-101">Enable-AzureRmAlias</span></span>

## <span data-ttu-id="7adb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7adb7-102">SYNOPSIS</span></span>
<span data-ttu-id="7adb7-103">Abilita gli alias dei prefissi di AzureRm per i moduli Az.</span><span class="sxs-lookup"><span data-stu-id="7adb7-103">Enables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="7adb7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7adb7-104">SYNTAX</span></span>

```
Enable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7adb7-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7adb7-105">DESCRIPTION</span></span>
<span data-ttu-id="7adb7-106">Abilita gli alias dei prefissi di AzureRm per i moduli Az.</span><span class="sxs-lookup"><span data-stu-id="7adb7-106">Enables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="7adb7-107">Se si specificato -Module, solo i moduli elencati avranno gli alias abilitati.</span><span class="sxs-lookup"><span data-stu-id="7adb7-107">If -Module is specified, only modules listed will have aliases enabled.</span></span> <span data-ttu-id="7adb7-108">In caso contrario, sono abilitati tutti gli alias di AzureRm.</span><span class="sxs-lookup"><span data-stu-id="7adb7-108">Otherwise all AzureRm aliases are enabled.</span></span>

## <span data-ttu-id="7adb7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7adb7-109">EXAMPLES</span></span>

### <span data-ttu-id="7adb7-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7adb7-110">Example 1</span></span>
```powershell
PS C:\> Enable-AzureRmAlias
```

<span data-ttu-id="7adb7-111">Abilita tutti i prefissi AzureRm per la sessione di PowerShell corrente.</span><span class="sxs-lookup"><span data-stu-id="7adb7-111">Enables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="7adb7-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7adb7-112">Example 2</span></span>
```powershell
PS C:\> Enable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="7adb7-113">Abilita gli alias AzureRm per il modulo Az.Accounts sia per il processo corrente che per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="7adb7-113">Enables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="7adb7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7adb7-114">PARAMETERS</span></span>

### <span data-ttu-id="7adb7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7adb7-115">-DefaultProfile</span></span>
<span data-ttu-id="7adb7-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7adb7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7adb7-117">-Module</span><span class="sxs-lookup"><span data-stu-id="7adb7-117">-Module</span></span>
<span data-ttu-id="7adb7-118">Indica per quali moduli abilitare gli alias.</span><span class="sxs-lookup"><span data-stu-id="7adb7-118">Indicates which modules to enable aliases for.</span></span>
<span data-ttu-id="7adb7-119">Se non ne viene specificato nessuno, il valore predefinito è tutti i moduli.</span><span class="sxs-lookup"><span data-stu-id="7adb7-119">If none are specified, default is all modules.</span></span>

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

### <span data-ttu-id="7adb7-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7adb7-120">-PassThru</span></span>
<span data-ttu-id="7adb7-121">Se specificato, il cmdlet restituirà tutti gli alias abilitati</span><span class="sxs-lookup"><span data-stu-id="7adb7-121">If specified, cmdlet will return all aliases enabled</span></span>

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

### <span data-ttu-id="7adb7-122">-Scope</span><span class="sxs-lookup"><span data-stu-id="7adb7-122">-Scope</span></span>
<span data-ttu-id="7adb7-123">Indica per quali alias dell'ambito deve essere abilitato.</span><span class="sxs-lookup"><span data-stu-id="7adb7-123">Indicates what scope aliases should be enabled for.</span></span> <span data-ttu-id="7adb7-124">L'impostazione predefinita è "Locale"</span><span class="sxs-lookup"><span data-stu-id="7adb7-124">Default is 'Local'</span></span>

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

### <span data-ttu-id="7adb7-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7adb7-125">-Confirm</span></span>
<span data-ttu-id="7adb7-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7adb7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7adb7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7adb7-127">-WhatIf</span></span>
<span data-ttu-id="7adb7-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7adb7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7adb7-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7adb7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7adb7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7adb7-130">CommonParameters</span></span>
<span data-ttu-id="7adb7-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7adb7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7adb7-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7adb7-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7adb7-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="7adb7-133">INPUTS</span></span>

### <span data-ttu-id="7adb7-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7adb7-134">None</span></span>

## <span data-ttu-id="7adb7-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7adb7-135">OUTPUTS</span></span>

### <span data-ttu-id="7adb7-136">System.String</span><span class="sxs-lookup"><span data-stu-id="7adb7-136">System.String</span></span>

## <span data-ttu-id="7adb7-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="7adb7-137">NOTES</span></span>

## <span data-ttu-id="7adb7-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7adb7-138">RELATED LINKS</span></span>

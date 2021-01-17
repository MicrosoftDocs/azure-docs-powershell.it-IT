---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
ms.openlocfilehash: 749507ba0bc0eec8aac7600c5262533ceb02a46b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367317"
---
# <span data-ttu-id="1099f-101">Disable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="1099f-101">Disable-AzureRmAlias</span></span>

## <span data-ttu-id="1099f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1099f-102">SYNOPSIS</span></span>
<span data-ttu-id="1099f-103">Disabilita gli alias di prefisso AzureRm per i moduli AZ.</span><span class="sxs-lookup"><span data-stu-id="1099f-103">Disables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="1099f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1099f-104">SYNTAX</span></span>

```
Disable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1099f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1099f-105">DESCRIPTION</span></span>
<span data-ttu-id="1099f-106">Disabilita gli alias di prefisso AzureRm per i moduli AZ.</span><span class="sxs-lookup"><span data-stu-id="1099f-106">Disables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="1099f-107">Se-Module è specificato, solo i moduli elencati avranno disabilitato alias.</span><span class="sxs-lookup"><span data-stu-id="1099f-107">If -Module is specified, only modules listed will have aliases disabled.</span></span> <span data-ttu-id="1099f-108">In caso contrario, tutti gli alias di AzureRm sono disabilitati.</span><span class="sxs-lookup"><span data-stu-id="1099f-108">Otherwise all AzureRm aliases are disabled.</span></span>

## <span data-ttu-id="1099f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1099f-109">EXAMPLES</span></span>

### <span data-ttu-id="1099f-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1099f-110">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias
```

<span data-ttu-id="1099f-111">Disabilita tutti i prefissi di AzureRm per la sessione corrente di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1099f-111">Disables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="1099f-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1099f-112">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="1099f-113">Disabilita gli alias di AzureRm per il modulo AZ. Accounts sia per il processo corrente che per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="1099f-113">Disables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="1099f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1099f-114">PARAMETERS</span></span>

### <span data-ttu-id="1099f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1099f-115">-DefaultProfile</span></span>
<span data-ttu-id="1099f-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1099f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1099f-117">-Module</span><span class="sxs-lookup"><span data-stu-id="1099f-117">-Module</span></span>
<span data-ttu-id="1099f-118">Indica i moduli per cui disabilitare gli alias.</span><span class="sxs-lookup"><span data-stu-id="1099f-118">Indicates which modules to disable aliases for.</span></span>
<span data-ttu-id="1099f-119">Se non si specifica nessuno, il valore predefinito è tutti i moduli abilitati.</span><span class="sxs-lookup"><span data-stu-id="1099f-119">If none are specified, default is all enabled modules.</span></span>

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

### <span data-ttu-id="1099f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1099f-120">-PassThru</span></span>
<span data-ttu-id="1099f-121">Se specificato, cmdlet restituirà tutti gli alias disabilitati</span><span class="sxs-lookup"><span data-stu-id="1099f-121">If specified, cmdlet will return all disabled aliases</span></span>

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

### <span data-ttu-id="1099f-122">-Ambito</span><span class="sxs-lookup"><span data-stu-id="1099f-122">-Scope</span></span>
<span data-ttu-id="1099f-123">Indica quali alias di ambito devono essere disabilitati.</span><span class="sxs-lookup"><span data-stu-id="1099f-123">Indicates what scope aliases should be disabled for.</span></span> <span data-ttu-id="1099f-124">Il valore predefinito è "processo"</span><span class="sxs-lookup"><span data-stu-id="1099f-124">Default is 'Process'</span></span>

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

### <span data-ttu-id="1099f-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1099f-125">-Confirm</span></span>
<span data-ttu-id="1099f-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1099f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1099f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1099f-127">-WhatIf</span></span>
<span data-ttu-id="1099f-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1099f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1099f-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1099f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1099f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1099f-130">CommonParameters</span></span>
<span data-ttu-id="1099f-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1099f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1099f-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1099f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1099f-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1099f-133">INPUTS</span></span>

### <span data-ttu-id="1099f-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1099f-134">None</span></span>

## <span data-ttu-id="1099f-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1099f-135">OUTPUTS</span></span>

### <span data-ttu-id="1099f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1099f-136">System.String</span></span>

## <span data-ttu-id="1099f-137">Note</span><span class="sxs-lookup"><span data-stu-id="1099f-137">NOTES</span></span>

## <span data-ttu-id="1099f-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1099f-138">RELATED LINKS</span></span>

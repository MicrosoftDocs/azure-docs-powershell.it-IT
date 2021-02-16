---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/register-azmigrateprojecttool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
ms.openlocfilehash: dff4b1b5ae83363a5a67cccbe70ee5c000af4419
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185078"
---
# <span data-ttu-id="6bcc4-101">Register-AzMigrateProjectTool</span><span class="sxs-lookup"><span data-stu-id="6bcc4-101">Register-AzMigrateProjectTool</span></span>

## <span data-ttu-id="6bcc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bcc4-102">SYNOPSIS</span></span>
<span data-ttu-id="6bcc4-103">Registra uno strumento nel progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="6bcc4-103">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="6bcc4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6bcc4-104">SYNTAX</span></span>

```
Register-AzMigrateProjectTool -MigrateProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AcceptLanguage <String>] [-Tool <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6bcc4-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6bcc4-105">DESCRIPTION</span></span>
<span data-ttu-id="6bcc4-106">Registra uno strumento nel progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="6bcc4-106">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="6bcc4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6bcc4-107">EXAMPLES</span></span>

### <span data-ttu-id="6bcc4-108">Esempio 1: Strumento REgister.</span><span class="sxs-lookup"><span data-stu-id="6bcc4-108">Example 1: REgister tool.</span></span>
```powershell
PS C:\> Register-AzMigrateProjectTool -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Tool Zerto

True
```

<span data-ttu-id="6bcc4-109">Registra uno strumento nel progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="6bcc4-109">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="6bcc4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6bcc4-110">PARAMETERS</span></span>

### <span data-ttu-id="6bcc4-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="6bcc4-111">-AcceptLanguage</span></span>
<span data-ttu-id="6bcc4-112">Intestazione di richiesta standard.</span><span class="sxs-lookup"><span data-stu-id="6bcc4-112">Standard request header.</span></span>
<span data-ttu-id="6bcc4-113">Usato dal servizio per rispondere al client nella lingua appropriata.</span><span class="sxs-lookup"><span data-stu-id="6bcc4-113">Used by service to respond to client in appropriate language.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bcc4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bcc4-114">-DefaultProfile</span></span>
<span data-ttu-id="6bcc4-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6bcc4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bcc4-116">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="6bcc4-116">-MigrateProjectName</span></span>
<span data-ttu-id="6bcc4-117">Nome del progetto Azure Migrate.</span><span class="sxs-lookup"><span data-stu-id="6bcc4-117">Name of the Azure Migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bcc4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bcc4-118">-ResourceGroupName</span></span>
<span data-ttu-id="6bcc4-119">Il nome del gruppo di risorse di Azure di cui viene eseguita la migrazione fa parte del progetto.</span><span class="sxs-lookup"><span data-stu-id="6bcc4-119">Name of the Azure Resource Group that migrate project is part of.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bcc4-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6bcc4-120">-SubscriptionId</span></span>
<span data-ttu-id="6bcc4-121">ID sottoscrizione di Azure in cui è stato creato il progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="6bcc4-121">Azure Subscription Id in which migrate project was created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bcc4-122">-Strumento</span><span class="sxs-lookup"><span data-stu-id="6bcc4-122">-Tool</span></span>
<span data-ttu-id="6bcc4-123">Ottiene o imposta lo strumento da registrare.</span><span class="sxs-lookup"><span data-stu-id="6bcc4-123">Gets or sets the tool to be registered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bcc4-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6bcc4-124">-Confirm</span></span>
<span data-ttu-id="6bcc4-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bcc4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bcc4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bcc4-126">-WhatIf</span></span>
<span data-ttu-id="6bcc4-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6bcc4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bcc4-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6bcc4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bcc4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bcc4-129">CommonParameters</span></span>
<span data-ttu-id="6bcc4-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bcc4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bcc4-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6bcc4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bcc4-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="6bcc4-132">INPUTS</span></span>

## <span data-ttu-id="6bcc4-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6bcc4-133">OUTPUTS</span></span>

### <span data-ttu-id="6bcc4-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6bcc4-134">System.Boolean</span></span>

## <span data-ttu-id="6bcc4-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="6bcc4-135">NOTES</span></span>

<span data-ttu-id="6bcc4-136">ALIAS</span><span class="sxs-lookup"><span data-stu-id="6bcc4-136">ALIASES</span></span>

## <span data-ttu-id="6bcc4-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6bcc4-137">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/register-azmigrateprojecttool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
ms.openlocfilehash: dff4b1b5ae83363a5a67cccbe70ee5c000af4419
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380698"
---
# <span data-ttu-id="ecc17-101">Register-AzMigrateProjectTool</span><span class="sxs-lookup"><span data-stu-id="ecc17-101">Register-AzMigrateProjectTool</span></span>

## <span data-ttu-id="ecc17-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ecc17-102">SYNOPSIS</span></span>
<span data-ttu-id="ecc17-103">Registra uno strumento con il progetto migra.</span><span class="sxs-lookup"><span data-stu-id="ecc17-103">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="ecc17-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ecc17-104">SYNTAX</span></span>

```
Register-AzMigrateProjectTool -MigrateProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AcceptLanguage <String>] [-Tool <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ecc17-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ecc17-105">DESCRIPTION</span></span>
<span data-ttu-id="ecc17-106">Registra uno strumento con il progetto migra.</span><span class="sxs-lookup"><span data-stu-id="ecc17-106">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="ecc17-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ecc17-107">EXAMPLES</span></span>

### <span data-ttu-id="ecc17-108">Esempio 1: strumento registra.</span><span class="sxs-lookup"><span data-stu-id="ecc17-108">Example 1: REgister tool.</span></span>
```powershell
PS C:\> Register-AzMigrateProjectTool -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Tool Zerto

True
```

<span data-ttu-id="ecc17-109">Registra uno strumento con il progetto migra.</span><span class="sxs-lookup"><span data-stu-id="ecc17-109">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="ecc17-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ecc17-110">PARAMETERS</span></span>

### <span data-ttu-id="ecc17-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="ecc17-111">-AcceptLanguage</span></span>
<span data-ttu-id="ecc17-112">Intestazione della richiesta standard.</span><span class="sxs-lookup"><span data-stu-id="ecc17-112">Standard request header.</span></span>
<span data-ttu-id="ecc17-113">Usato da Service per rispondere al client in una lingua appropriata.</span><span class="sxs-lookup"><span data-stu-id="ecc17-113">Used by service to respond to client in appropriate language.</span></span>

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

### <span data-ttu-id="ecc17-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecc17-114">-DefaultProfile</span></span>
<span data-ttu-id="ecc17-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ecc17-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecc17-116">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="ecc17-116">-MigrateProjectName</span></span>
<span data-ttu-id="ecc17-117">Nome del progetto di migrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ecc17-117">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="ecc17-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecc17-118">-ResourceGroupName</span></span>
<span data-ttu-id="ecc17-119">Il nome del gruppo di risorse di Azure in cui viene eseguita la migrazione di Project fa parte.</span><span class="sxs-lookup"><span data-stu-id="ecc17-119">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="ecc17-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ecc17-120">-SubscriptionId</span></span>
<span data-ttu-id="ecc17-121">ID sottoscrizione di Azure in cui è stata creata la migrazione del progetto.</span><span class="sxs-lookup"><span data-stu-id="ecc17-121">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="ecc17-122">-Strumento</span><span class="sxs-lookup"><span data-stu-id="ecc17-122">-Tool</span></span>
<span data-ttu-id="ecc17-123">Ottiene o imposta lo strumento da registrare.</span><span class="sxs-lookup"><span data-stu-id="ecc17-123">Gets or sets the tool to be registered.</span></span>

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

### <span data-ttu-id="ecc17-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ecc17-124">-Confirm</span></span>
<span data-ttu-id="ecc17-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecc17-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecc17-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecc17-126">-WhatIf</span></span>
<span data-ttu-id="ecc17-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ecc17-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecc17-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ecc17-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecc17-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecc17-129">CommonParameters</span></span>
<span data-ttu-id="ecc17-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecc17-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecc17-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ecc17-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecc17-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ecc17-132">INPUTS</span></span>

## <span data-ttu-id="ecc17-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ecc17-133">OUTPUTS</span></span>

### <span data-ttu-id="ecc17-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ecc17-134">System.Boolean</span></span>

## <span data-ttu-id="ecc17-135">Note</span><span class="sxs-lookup"><span data-stu-id="ecc17-135">NOTES</span></span>

<span data-ttu-id="ecc17-136">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ecc17-136">ALIASES</span></span>

## <span data-ttu-id="ecc17-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ecc17-137">RELATED LINKS</span></span>


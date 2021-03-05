---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/remove-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
ms.openlocfilehash: d9edb00bf7944400fa681f857dd7005d9eaf69b5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003757"
---
# <span data-ttu-id="25402-101">Remove-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="25402-101">Remove-AzMigrateProject</span></span>

## <span data-ttu-id="25402-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25402-102">SYNOPSIS</span></span>
<span data-ttu-id="25402-103">Eliminare il progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="25402-103">Delete the migrate project.</span></span>
<span data-ttu-id="25402-104">L'eliminazione di un progetto inesistente non è un'operazione.</span><span class="sxs-lookup"><span data-stu-id="25402-104">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="25402-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="25402-105">SYNTAX</span></span>

```
Remove-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="25402-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="25402-106">DESCRIPTION</span></span>
<span data-ttu-id="25402-107">Eliminare il progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="25402-107">Delete the migrate project.</span></span>
<span data-ttu-id="25402-108">L'eliminazione di un progetto inesistente non è un'operazione.</span><span class="sxs-lookup"><span data-stu-id="25402-108">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="25402-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="25402-109">EXAMPLES</span></span>

### <span data-ttu-id="25402-110">Esempio 1: Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="25402-110">Example 1: Delete (Default)</span></span>
```powershell
PS C:\> Remove-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

--No output--
```

<span data-ttu-id="25402-111">Eliminare il progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="25402-111">Delete the migrate project.</span></span>
<span data-ttu-id="25402-112">L'eliminazione di un progetto inesistente non è un'operazione.</span><span class="sxs-lookup"><span data-stu-id="25402-112">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="25402-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25402-113">PARAMETERS</span></span>

### <span data-ttu-id="25402-114">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="25402-114">-AcceptLanguage</span></span>
<span data-ttu-id="25402-115">Intestazione di richiesta standard.</span><span class="sxs-lookup"><span data-stu-id="25402-115">Standard request header.</span></span>
<span data-ttu-id="25402-116">Usato dal servizio per rispondere al client nella lingua appropriata.</span><span class="sxs-lookup"><span data-stu-id="25402-116">Used by service to respond to client in appropriate language.</span></span>

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

### <span data-ttu-id="25402-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25402-117">-DefaultProfile</span></span>
<span data-ttu-id="25402-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="25402-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25402-119">-Name</span><span class="sxs-lookup"><span data-stu-id="25402-119">-Name</span></span>
<span data-ttu-id="25402-120">Nome del progetto Azure Migrate.</span><span class="sxs-lookup"><span data-stu-id="25402-120">Name of the Azure Migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MigrateProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25402-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25402-121">-PassThru</span></span>
<span data-ttu-id="25402-122">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="25402-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="25402-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25402-123">-ResourceGroupName</span></span>
<span data-ttu-id="25402-124">Il nome del gruppo di risorse di Azure di cui viene eseguita la migrazione fa parte del progetto.</span><span class="sxs-lookup"><span data-stu-id="25402-124">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="25402-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="25402-125">-SubscriptionId</span></span>
<span data-ttu-id="25402-126">ID sottoscrizione di Azure in cui è stato creato il progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="25402-126">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="25402-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25402-127">-Confirm</span></span>
<span data-ttu-id="25402-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25402-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25402-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25402-129">-WhatIf</span></span>
<span data-ttu-id="25402-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="25402-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25402-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="25402-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25402-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25402-132">CommonParameters</span></span>
<span data-ttu-id="25402-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25402-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25402-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="25402-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25402-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="25402-135">INPUTS</span></span>

## <span data-ttu-id="25402-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="25402-136">OUTPUTS</span></span>

### <span data-ttu-id="25402-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="25402-137">System.Boolean</span></span>

## <span data-ttu-id="25402-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="25402-138">NOTES</span></span>

<span data-ttu-id="25402-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="25402-139">ALIASES</span></span>

## <span data-ttu-id="25402-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="25402-140">RELATED LINKS</span></span>


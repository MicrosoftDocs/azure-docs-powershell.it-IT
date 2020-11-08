---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/remove-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
ms.openlocfilehash: e0918573b7fc1190d32aaaaa4bfe73ed9fe05fe6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202090"
---
# <span data-ttu-id="85f36-101">Remove-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="85f36-101">Remove-AzMigrateProject</span></span>

## <span data-ttu-id="85f36-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="85f36-102">SYNOPSIS</span></span>
<span data-ttu-id="85f36-103">Eliminare il progetto migra.</span><span class="sxs-lookup"><span data-stu-id="85f36-103">Delete the migrate project.</span></span>
<span data-ttu-id="85f36-104">L'eliminazione di un progetto inesistente è un'operazione non operativa.</span><span class="sxs-lookup"><span data-stu-id="85f36-104">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="85f36-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85f36-105">SYNTAX</span></span>

```
Remove-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="85f36-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85f36-106">DESCRIPTION</span></span>
<span data-ttu-id="85f36-107">Eliminare il progetto migra.</span><span class="sxs-lookup"><span data-stu-id="85f36-107">Delete the migrate project.</span></span>
<span data-ttu-id="85f36-108">L'eliminazione di un progetto inesistente è un'operazione non operativa.</span><span class="sxs-lookup"><span data-stu-id="85f36-108">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="85f36-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85f36-109">EXAMPLES</span></span>

### <span data-ttu-id="85f36-110">Esempio 1: Delete (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="85f36-110">Example 1: Delete (Default)</span></span>
```powershell
PS C:\> Remove-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

--No output--
```

<span data-ttu-id="85f36-111">Eliminare il progetto migra.</span><span class="sxs-lookup"><span data-stu-id="85f36-111">Delete the migrate project.</span></span>
<span data-ttu-id="85f36-112">L'eliminazione di un progetto inesistente è un'operazione non operativa.</span><span class="sxs-lookup"><span data-stu-id="85f36-112">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="85f36-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="85f36-113">PARAMETERS</span></span>

### <span data-ttu-id="85f36-114">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="85f36-114">-AcceptLanguage</span></span>
<span data-ttu-id="85f36-115">Intestazione della richiesta standard.</span><span class="sxs-lookup"><span data-stu-id="85f36-115">Standard request header.</span></span>
<span data-ttu-id="85f36-116">Usato da Service per rispondere al client in una lingua appropriata.</span><span class="sxs-lookup"><span data-stu-id="85f36-116">Used by service to respond to client in appropriate language.</span></span>

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

### <span data-ttu-id="85f36-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85f36-117">-DefaultProfile</span></span>
<span data-ttu-id="85f36-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="85f36-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85f36-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="85f36-119">-Name</span></span>
<span data-ttu-id="85f36-120">Nome del progetto di migrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="85f36-120">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="85f36-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85f36-121">-PassThru</span></span>
<span data-ttu-id="85f36-122">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="85f36-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="85f36-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85f36-123">-ResourceGroupName</span></span>
<span data-ttu-id="85f36-124">Il nome del gruppo di risorse di Azure in cui viene eseguita la migrazione di Project fa parte.</span><span class="sxs-lookup"><span data-stu-id="85f36-124">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="85f36-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="85f36-125">-SubscriptionId</span></span>
<span data-ttu-id="85f36-126">ID sottoscrizione di Azure in cui è stata creata la migrazione del progetto.</span><span class="sxs-lookup"><span data-stu-id="85f36-126">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="85f36-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="85f36-127">-Confirm</span></span>
<span data-ttu-id="85f36-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85f36-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85f36-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85f36-129">-WhatIf</span></span>
<span data-ttu-id="85f36-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85f36-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85f36-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85f36-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85f36-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85f36-132">CommonParameters</span></span>
<span data-ttu-id="85f36-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85f36-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85f36-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85f36-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85f36-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="85f36-135">INPUTS</span></span>

## <span data-ttu-id="85f36-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85f36-136">OUTPUTS</span></span>

### <span data-ttu-id="85f36-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="85f36-137">System.Boolean</span></span>

## <span data-ttu-id="85f36-138">Note</span><span class="sxs-lookup"><span data-stu-id="85f36-138">NOTES</span></span>

<span data-ttu-id="85f36-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="85f36-139">ALIASES</span></span>

## <span data-ttu-id="85f36-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85f36-140">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/new-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
ms.openlocfilehash: 8b3a14c9e8416c1ffc9809d09d664b7809f53a1d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982686"
---
# <span data-ttu-id="507a7-101">New-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="507a7-101">New-AzMigrateProject</span></span>

## <span data-ttu-id="507a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="507a7-102">SYNOPSIS</span></span>
<span data-ttu-id="507a7-103">Crea un nuovo progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="507a7-103">Creates a new Migrate project.</span></span>

## <span data-ttu-id="507a7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="507a7-104">SYNTAX</span></span>

```
New-AzMigrateProject -Location <String> -Name <String> -ResourceGroupName <String> [-ETag <String>]
 [-Property <IMigrateProjectProperties>] [-SubscriptionId <String>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="507a7-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="507a7-105">DESCRIPTION</span></span>
<span data-ttu-id="507a7-106">Crea un nuovo progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="507a7-106">Creates a new Migrate project.</span></span>

## <span data-ttu-id="507a7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="507a7-107">EXAMPLES</span></span>

### <span data-ttu-id="507a7-108">Esempio 1: Creare (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="507a7-108">Example 1: Create (Default)</span></span>
```powershell
PS C:\> New-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName kuchaturimpkocrg1 -Name kuchaturimpkocrg1pwshp14 -Location "centralus"

ETag Location  Name                     Type
---- --------  ----                     ----
     centralus kuchaturimpkocrg1pwshp14 Microsoft.Migrate/MigrateProjects

```

<span data-ttu-id="507a7-109">Metodo per creare un nuovo progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="507a7-109">Method to create a new migrate project.</span></span>

## <span data-ttu-id="507a7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="507a7-110">PARAMETERS</span></span>

### <span data-ttu-id="507a7-111">-ETag</span><span class="sxs-lookup"><span data-stu-id="507a7-111">-ETag</span></span>
<span data-ttu-id="507a7-112">Specifica il nome del computer VMware.</span><span class="sxs-lookup"><span data-stu-id="507a7-112">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="507a7-113">-Location</span><span class="sxs-lookup"><span data-stu-id="507a7-113">-Location</span></span>
<span data-ttu-id="507a7-114">Specifica il nome del computer VMware.</span><span class="sxs-lookup"><span data-stu-id="507a7-114">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="507a7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="507a7-115">-Name</span></span>
<span data-ttu-id="507a7-116">Specifica il nome del progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="507a7-116">Specifies the migrate project name.</span></span>

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

### <span data-ttu-id="507a7-117">-Proprietà</span><span class="sxs-lookup"><span data-stu-id="507a7-117">-Property</span></span>
<span data-ttu-id="507a7-118">Specifica le proprietà del progetto.</span><span class="sxs-lookup"><span data-stu-id="507a7-118">Specifies the project properties.</span></span>
<span data-ttu-id="507a7-119">Per creare, vedere la sezione NOTE per le proprietà PROPERTY e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="507a7-119">To construct, see NOTES section for PROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProjectProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="507a7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="507a7-120">-ResourceGroupName</span></span>
<span data-ttu-id="507a7-121">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="507a7-121">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="507a7-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="507a7-122">-SubscriptionId</span></span>
<span data-ttu-id="507a7-123">Specifica l'ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="507a7-123">Specifies the subscription id.</span></span>

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

### <span data-ttu-id="507a7-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="507a7-124">-Confirm</span></span>
<span data-ttu-id="507a7-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="507a7-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="507a7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="507a7-126">-WhatIf</span></span>
<span data-ttu-id="507a7-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="507a7-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="507a7-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="507a7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="507a7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="507a7-129">CommonParameters</span></span>
<span data-ttu-id="507a7-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="507a7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="507a7-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="507a7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="507a7-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="507a7-132">INPUTS</span></span>

## <span data-ttu-id="507a7-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="507a7-133">OUTPUTS</span></span>

## <span data-ttu-id="507a7-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="507a7-134">NOTES</span></span>

<span data-ttu-id="507a7-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="507a7-135">ALIASES</span></span>

<span data-ttu-id="507a7-136">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="507a7-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="507a7-137">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="507a7-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="507a7-138">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="507a7-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="507a7-139">PROPRIETÀ: <IMigrateProjectProperties> specifica le proprietà del progetto.</span><span class="sxs-lookup"><span data-stu-id="507a7-139">PROPERTY <IMigrateProjectProperties>: Specifies the project properties.</span></span>
  - <span data-ttu-id="507a7-140">`[ProvisioningState <ProvisioningState?>]`: stato di provisioning del progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="507a7-140">`[ProvisioningState <ProvisioningState?>]`: Provisioning state of the migrate project.</span></span>
  - <span data-ttu-id="507a7-141">`[RegisteredTool <String[]>]`: ottiene o imposta l'elenco di strumenti registrati con il progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="507a7-141">`[RegisteredTool <String[]>]`: Gets or sets the list of tools registered with the migrate project.</span></span>

## <span data-ttu-id="507a7-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="507a7-142">RELATED LINKS</span></span>


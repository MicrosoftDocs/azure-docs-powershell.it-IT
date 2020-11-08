---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
ms.openlocfilehash: 32c4799f574e94eecee1f7ebf810c2f27bc5eccf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202326"
---
# <span data-ttu-id="adc2c-101">New-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="adc2c-101">New-AzMigrateProject</span></span>

## <span data-ttu-id="adc2c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="adc2c-102">SYNOPSIS</span></span>
<span data-ttu-id="adc2c-103">Crea un nuovo progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="adc2c-103">Creates a new Migrate project.</span></span>

## <span data-ttu-id="adc2c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="adc2c-104">SYNTAX</span></span>

```
New-AzMigrateProject -Location <String> -Name <String> -ResourceGroupName <String> [-ETag <String>]
 [-Property <IMigrateProjectProperties>] [-SubscriptionId <String>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="adc2c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="adc2c-105">DESCRIPTION</span></span>
<span data-ttu-id="adc2c-106">Crea un nuovo progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="adc2c-106">Creates a new Migrate project.</span></span>

## <span data-ttu-id="adc2c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="adc2c-107">EXAMPLES</span></span>

### <span data-ttu-id="adc2c-108">Esempio 1: creare (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="adc2c-108">Example 1: Create (Default)</span></span>
```powershell
PS C:\> New-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName kuchaturimpkocrg1 -Name kuchaturimpkocrg1pwshp14 -Location "centralus"

ETag Location  Name                     Type
---- --------  ----                     ----
     centralus kuchaturimpkocrg1pwshp14 Microsoft.Migrate/MigrateProjects

```

<span data-ttu-id="adc2c-109">Metodo per creare un nuovo progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="adc2c-109">Method to create a new migrate project.</span></span>

## <span data-ttu-id="adc2c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="adc2c-110">PARAMETERS</span></span>

### <span data-ttu-id="adc2c-111">-ETag</span><span class="sxs-lookup"><span data-stu-id="adc2c-111">-ETag</span></span>
<span data-ttu-id="adc2c-112">Specifica il nome del computer VMware.</span><span class="sxs-lookup"><span data-stu-id="adc2c-112">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="adc2c-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="adc2c-113">-Location</span></span>
<span data-ttu-id="adc2c-114">Specifica il nome del computer VMware.</span><span class="sxs-lookup"><span data-stu-id="adc2c-114">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="adc2c-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="adc2c-115">-Name</span></span>
<span data-ttu-id="adc2c-116">Specifica il nome della migrazione del progetto.</span><span class="sxs-lookup"><span data-stu-id="adc2c-116">Specifies the migrate project name.</span></span>

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

### <span data-ttu-id="adc2c-117">-Property</span><span class="sxs-lookup"><span data-stu-id="adc2c-117">-Property</span></span>
<span data-ttu-id="adc2c-118">Specifica le proprietà del progetto.</span><span class="sxs-lookup"><span data-stu-id="adc2c-118">Specifies the project properties.</span></span>
<span data-ttu-id="adc2c-119">Per costruire, vedere la sezione Note per le proprietà delle proprietà e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="adc2c-119">To construct, see NOTES section for PROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="adc2c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adc2c-120">-ResourceGroupName</span></span>
<span data-ttu-id="adc2c-121">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="adc2c-121">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="adc2c-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="adc2c-122">-SubscriptionId</span></span>
<span data-ttu-id="adc2c-123">Specifica l'ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="adc2c-123">Specifies the subscription id.</span></span>

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

### <span data-ttu-id="adc2c-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="adc2c-124">-Confirm</span></span>
<span data-ttu-id="adc2c-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adc2c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adc2c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adc2c-126">-WhatIf</span></span>
<span data-ttu-id="adc2c-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="adc2c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adc2c-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="adc2c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adc2c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adc2c-129">CommonParameters</span></span>
<span data-ttu-id="adc2c-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adc2c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adc2c-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="adc2c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adc2c-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="adc2c-132">INPUTS</span></span>

## <span data-ttu-id="adc2c-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="adc2c-133">OUTPUTS</span></span>

## <span data-ttu-id="adc2c-134">Note</span><span class="sxs-lookup"><span data-stu-id="adc2c-134">NOTES</span></span>

<span data-ttu-id="adc2c-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="adc2c-135">ALIASES</span></span>

<span data-ttu-id="adc2c-136">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="adc2c-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="adc2c-137">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="adc2c-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="adc2c-138">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="adc2c-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="adc2c-139">PROPRIETÀ <IMigrateProjectProperties> : specifica le proprietà del progetto.</span><span class="sxs-lookup"><span data-stu-id="adc2c-139">PROPERTY <IMigrateProjectProperties>: Specifies the project properties.</span></span>
  - <span data-ttu-id="adc2c-140">`[ProvisioningState <ProvisioningState?>]`: Provisioning dello stato del progetto migra.</span><span class="sxs-lookup"><span data-stu-id="adc2c-140">`[ProvisioningState <ProvisioningState?>]`: Provisioning state of the migrate project.</span></span>
  - <span data-ttu-id="adc2c-141">`[RegisteredTool <String[]>]`: Ottiene o imposta l'elenco di strumenti registrati con il progetto migra.</span><span class="sxs-lookup"><span data-stu-id="adc2c-141">`[RegisteredTool <String[]>]`: Gets or sets the list of tools registered with the migrate project.</span></span>

## <span data-ttu-id="adc2c-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="adc2c-142">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/remove-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
ms.openlocfilehash: 5f212240eaee9ebc46fd7d5cde2ee2e2ec311ac2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475247"
---
# <span data-ttu-id="c8968-101">Remove-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8968-101">Remove-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="c8968-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c8968-102">SYNOPSIS</span></span>
<span data-ttu-id="c8968-103">Eliminare il record di configurazione</span><span class="sxs-lookup"><span data-stu-id="c8968-103">Delete Configuration record</span></span>

## <span data-ttu-id="c8968-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c8968-104">SYNTAX</span></span>

```
Remove-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8968-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8968-105">DESCRIPTION</span></span>
<span data-ttu-id="c8968-106">Eliminare il record di configurazione della manutenzione</span><span class="sxs-lookup"><span data-stu-id="c8968-106">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="c8968-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c8968-107">EXAMPLES</span></span>

### <span data-ttu-id="c8968-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c8968-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus

Remove-AzMaintenanceConfiguration operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="c8968-109">Eliminare il record di configurazione della manutenzione</span><span class="sxs-lookup"><span data-stu-id="c8968-109">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="c8968-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c8968-110">PARAMETERS</span></span>

### <span data-ttu-id="c8968-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8968-111">-AsJob</span></span>
<span data-ttu-id="c8968-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c8968-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c8968-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8968-113">-DefaultProfile</span></span>
<span data-ttu-id="c8968-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c8968-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8968-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c8968-115">-Force</span></span>
<span data-ttu-id="c8968-116">Forza Rimuovi senza conferma.</span><span class="sxs-lookup"><span data-stu-id="c8968-116">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="c8968-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="c8968-117">-Name</span></span>
<span data-ttu-id="c8968-118">Nome della configurazione della manutenzione.</span><span class="sxs-lookup"><span data-stu-id="c8968-118">The maintenance configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8968-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8968-119">-PassThru</span></span>
<span data-ttu-id="c8968-120">Restituisce lo stato dell'operazione Remove.</span><span class="sxs-lookup"><span data-stu-id="c8968-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="c8968-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="c8968-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c8968-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8968-122">-ResourceGroupName</span></span>
<span data-ttu-id="c8968-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c8968-123">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8968-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c8968-124">-Confirm</span></span>
<span data-ttu-id="c8968-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8968-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8968-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8968-126">-WhatIf</span></span>
<span data-ttu-id="c8968-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8968-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8968-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8968-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8968-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8968-129">CommonParameters</span></span>
<span data-ttu-id="c8968-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8968-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8968-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8968-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8968-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c8968-132">INPUTS</span></span>

### <span data-ttu-id="c8968-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c8968-133">System.String</span></span>

## <span data-ttu-id="c8968-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c8968-134">OUTPUTS</span></span>

### <span data-ttu-id="c8968-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c8968-135">System.Boolean</span></span>

## <span data-ttu-id="c8968-136">Note</span><span class="sxs-lookup"><span data-stu-id="c8968-136">NOTES</span></span>

## <span data-ttu-id="c8968-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c8968-137">RELATED LINKS</span></span>

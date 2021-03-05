---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/remove-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
ms.openlocfilehash: 2cebdeab994926d51ff5ff49e6a4a101f3e5c778
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985947"
---
# <span data-ttu-id="88b93-101">Remove-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="88b93-101">Remove-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="88b93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88b93-102">SYNOPSIS</span></span>
<span data-ttu-id="88b93-103">Elimina record di configurazione</span><span class="sxs-lookup"><span data-stu-id="88b93-103">Delete Configuration record</span></span>

## <span data-ttu-id="88b93-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="88b93-104">SYNTAX</span></span>

```
Remove-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88b93-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="88b93-105">DESCRIPTION</span></span>
<span data-ttu-id="88b93-106">Elimina record Configurazione manutenzione</span><span class="sxs-lookup"><span data-stu-id="88b93-106">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="88b93-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="88b93-107">EXAMPLES</span></span>

### <span data-ttu-id="88b93-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="88b93-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus

Remove-AzMaintenanceConfiguration operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="88b93-109">Elimina record Configurazione manutenzione</span><span class="sxs-lookup"><span data-stu-id="88b93-109">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="88b93-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88b93-110">PARAMETERS</span></span>

### <span data-ttu-id="88b93-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88b93-111">-AsJob</span></span>
<span data-ttu-id="88b93-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="88b93-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="88b93-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88b93-113">-DefaultProfile</span></span>
<span data-ttu-id="88b93-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="88b93-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88b93-115">-Force</span><span class="sxs-lookup"><span data-stu-id="88b93-115">-Force</span></span>
<span data-ttu-id="88b93-116">Forzare la rimozione senza conferma.</span><span class="sxs-lookup"><span data-stu-id="88b93-116">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="88b93-117">-Name</span><span class="sxs-lookup"><span data-stu-id="88b93-117">-Name</span></span>
<span data-ttu-id="88b93-118">Nome della configurazione di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="88b93-118">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="88b93-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88b93-119">-PassThru</span></span>
<span data-ttu-id="88b93-120">Restituisce lo stato dell'operazione Remove.</span><span class="sxs-lookup"><span data-stu-id="88b93-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="88b93-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="88b93-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="88b93-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88b93-122">-ResourceGroupName</span></span>
<span data-ttu-id="88b93-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="88b93-123">The resource Group Name.</span></span>

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

### <span data-ttu-id="88b93-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88b93-124">-Confirm</span></span>
<span data-ttu-id="88b93-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88b93-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88b93-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88b93-126">-WhatIf</span></span>
<span data-ttu-id="88b93-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="88b93-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88b93-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="88b93-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88b93-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88b93-129">CommonParameters</span></span>
<span data-ttu-id="88b93-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88b93-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88b93-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="88b93-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88b93-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="88b93-132">INPUTS</span></span>

### <span data-ttu-id="88b93-133">System.String</span><span class="sxs-lookup"><span data-stu-id="88b93-133">System.String</span></span>

## <span data-ttu-id="88b93-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="88b93-134">OUTPUTS</span></span>

### <span data-ttu-id="88b93-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="88b93-135">System.Boolean</span></span>

## <span data-ttu-id="88b93-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="88b93-136">NOTES</span></span>

## <span data-ttu-id="88b93-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="88b93-137">RELATED LINKS</span></span>

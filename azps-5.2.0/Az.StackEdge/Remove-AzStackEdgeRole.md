---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeRole.md
ms.openlocfilehash: 7e462c7f6d22a071217a7279a44114c3a95504bd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358735"
---
# <span data-ttu-id="84d90-101">Remove-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="84d90-101">Remove-AzStackEdgeRole</span></span>

## <span data-ttu-id="84d90-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="84d90-102">SYNOPSIS</span></span>
<span data-ttu-id="84d90-103">Rimuove il ruolo di sacco associato per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="84d90-103">Removes the associated IoT role for a device.</span></span>

## <span data-ttu-id="84d90-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84d90-104">SYNTAX</span></span>

### <span data-ttu-id="84d90-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="84d90-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84d90-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="84d90-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeRole -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84d90-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84d90-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeRole -InputObject <PSStackEdgeRole> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84d90-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84d90-108">DESCRIPTION</span></span>
<span data-ttu-id="84d90-109">Il cmdlet **Remove-AzStackEdgeRole** rimuove il ruolo di un sacco associato per un dispositivo Edge dello stack.</span><span class="sxs-lookup"><span data-stu-id="84d90-109">The **Remove-AzStackEdgeRole** cmdlet removes the associated IoT role for a Stack Edge device.</span></span>

## <span data-ttu-id="84d90-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84d90-110">EXAMPLES</span></span>

### <span data-ttu-id="84d90-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="84d90-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleName
```

## <span data-ttu-id="84d90-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="84d90-112">PARAMETERS</span></span>

### <span data-ttu-id="84d90-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="84d90-113">-AsJob</span></span>
<span data-ttu-id="84d90-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="84d90-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="84d90-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84d90-115">-DefaultProfile</span></span>
<span data-ttu-id="84d90-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="84d90-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84d90-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="84d90-117">-DeviceName</span></span>
<span data-ttu-id="84d90-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="84d90-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84d90-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84d90-119">-InputObject</span></span>
<span data-ttu-id="84d90-120">Oggetto di input</span><span class="sxs-lookup"><span data-stu-id="84d90-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84d90-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="84d90-121">-Name</span></span>
<span data-ttu-id="84d90-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="84d90-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84d90-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84d90-123">-PassThru</span></span>
<span data-ttu-id="84d90-124">Restituisce vero in caso di esito positivo</span><span class="sxs-lookup"><span data-stu-id="84d90-124">returns true if successful</span></span>

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

### <span data-ttu-id="84d90-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84d90-125">-ResourceGroupName</span></span>
<span data-ttu-id="84d90-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="84d90-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84d90-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84d90-127">-ResourceId</span></span>
<span data-ttu-id="84d90-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="84d90-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84d90-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="84d90-129">-Confirm</span></span>
<span data-ttu-id="84d90-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84d90-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84d90-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84d90-131">-WhatIf</span></span>
<span data-ttu-id="84d90-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84d90-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="84d90-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84d90-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84d90-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84d90-134">CommonParameters</span></span>
<span data-ttu-id="84d90-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84d90-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84d90-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84d90-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84d90-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="84d90-137">INPUTS</span></span>

### <span data-ttu-id="84d90-138">System. String</span><span class="sxs-lookup"><span data-stu-id="84d90-138">System.String</span></span>

### <span data-ttu-id="84d90-139">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="84d90-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="84d90-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84d90-140">OUTPUTS</span></span>

### <span data-ttu-id="84d90-141">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="84d90-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="84d90-142">Note</span><span class="sxs-lookup"><span data-stu-id="84d90-142">NOTES</span></span>

## <span data-ttu-id="84d90-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84d90-143">RELATED LINKS</span></span>

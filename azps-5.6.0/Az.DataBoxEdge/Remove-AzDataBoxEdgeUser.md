---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/remove-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
ms.openlocfilehash: 8c977c61f332ccdc927dd3f0e070d635e6095acf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983245"
---
# <span data-ttu-id="c60ac-101">Remove-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="c60ac-101">Remove-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="c60ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c60ac-102">SYNOPSIS</span></span>
<span data-ttu-id="c60ac-103">Rimuove un utente da un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c60ac-103">Removes a user on a device.</span></span>

## <span data-ttu-id="c60ac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c60ac-104">SYNTAX</span></span>

### <span data-ttu-id="c60ac-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c60ac-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c60ac-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c60ac-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c60ac-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c60ac-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-InputObject] <PSDataBoxEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c60ac-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c60ac-108">DESCRIPTION</span></span>
<span data-ttu-id="c60ac-109">Il cmdlet **Remove-AzDataBoxEdgeUser** rimuove un utente dal dispositivo Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="c60ac-109">The **Remove-AzDataBoxEdgeUser** cmdlet removes a user on the Data Box Edge device.</span></span> <span data-ttu-id="c60ac-110">È supportata la creazione solo di `Share` utenti di tipo.</span><span class="sxs-lookup"><span data-stu-id="c60ac-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="c60ac-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c60ac-111">EXAMPLES</span></span>

### <span data-ttu-id="c60ac-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c60ac-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="c60ac-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c60ac-113">PARAMETERS</span></span>

### <span data-ttu-id="c60ac-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c60ac-114">-AsJob</span></span>
<span data-ttu-id="c60ac-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c60ac-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c60ac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c60ac-116">-DefaultProfile</span></span>
<span data-ttu-id="c60ac-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c60ac-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c60ac-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="c60ac-118">-DeviceName</span></span>
<span data-ttu-id="c60ac-119">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="c60ac-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c60ac-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c60ac-120">-InputObject</span></span>
<span data-ttu-id="c60ac-121">Oggetto Input</span><span class="sxs-lookup"><span data-stu-id="c60ac-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c60ac-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c60ac-122">-Name</span></span>
<span data-ttu-id="c60ac-123">Nome utente</span><span class="sxs-lookup"><span data-stu-id="c60ac-123">Username</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c60ac-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c60ac-124">-PassThru</span></span>
<span data-ttu-id="c60ac-125">restituisce true se ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="c60ac-125">returns true if successful</span></span>

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

### <span data-ttu-id="c60ac-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c60ac-126">-ResourceGroupName</span></span>
<span data-ttu-id="c60ac-127">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="c60ac-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c60ac-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c60ac-128">-ResourceId</span></span>
<span data-ttu-id="c60ac-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="c60ac-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c60ac-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c60ac-130">-Confirm</span></span>
<span data-ttu-id="c60ac-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c60ac-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c60ac-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c60ac-132">-WhatIf</span></span>
<span data-ttu-id="c60ac-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c60ac-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c60ac-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c60ac-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c60ac-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c60ac-135">CommonParameters</span></span>
<span data-ttu-id="c60ac-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c60ac-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c60ac-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c60ac-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c60ac-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="c60ac-138">INPUTS</span></span>

### <span data-ttu-id="c60ac-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c60ac-139">System.String</span></span>

### <span data-ttu-id="c60ac-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="c60ac-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="c60ac-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c60ac-141">OUTPUTS</span></span>

### <span data-ttu-id="c60ac-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="c60ac-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="c60ac-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="c60ac-143">NOTES</span></span>

## <span data-ttu-id="c60ac-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c60ac-144">RELATED LINKS</span></span>

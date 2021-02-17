---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroup.md
ms.openlocfilehash: 895974f12c7472cb93679cb27ca895ca40757f53
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178775"
---
# <span data-ttu-id="b61d8-101">Remove-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="b61d8-101">Remove-AzADGroup</span></span>

## <span data-ttu-id="b61d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b61d8-102">SYNOPSIS</span></span>
<span data-ttu-id="b61d8-103">Elimina un gruppo di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b61d8-103">Deletes an active directory group.</span></span>

## <span data-ttu-id="b61d8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b61d8-104">SYNTAX</span></span>

### <span data-ttu-id="b61d8-105">ObjectIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b61d8-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADGroup -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b61d8-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b61d8-106">DisplayNameParameterSet</span></span>
```
Remove-AzADGroup -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b61d8-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b61d8-107">InputObjectParameterSet</span></span>
```
Remove-AzADGroup -InputObject <PSADGroup> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b61d8-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b61d8-108">DESCRIPTION</span></span>
<span data-ttu-id="b61d8-109">Elimina un gruppo di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b61d8-109">Deletes an active directory group.</span></span>

## <span data-ttu-id="b61d8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b61d8-110">EXAMPLES</span></span>

### <span data-ttu-id="b61d8-111">Esempio 1: Rimuovere un gruppo per ID oggetto</span><span class="sxs-lookup"><span data-stu-id="b61d8-111">Example 1: Remove a group by object id</span></span>

```powershell
PS C:\> Remove-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="b61d8-112">Rimuove il gruppo con ID oggetto '85F89C90-780E-4AA6-9F4F-6F268D322EEE' dal tenant.</span><span class="sxs-lookup"><span data-stu-id="b61d8-112">Removes the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' from the tenant.</span></span>

### <span data-ttu-id="b61d8-113">Esempio 2: Rimuovere un gruppo tramite piping</span><span class="sxs-lookup"><span data-stu-id="b61d8-113">Example 2: Remove a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroup
```

<span data-ttu-id="b61d8-114">Ottiene il gruppo con ID oggetto '85F89C90-780E-4AA6-9F4F-6F268D322EEE' e pipe che a Remove-AzADGroup per rimuovere il gruppo dal tenant.</span><span class="sxs-lookup"><span data-stu-id="b61d8-114">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes that to Remove-AzADGroup to remove the group from the tenant.</span></span>

## <span data-ttu-id="b61d8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b61d8-115">PARAMETERS</span></span>

### <span data-ttu-id="b61d8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b61d8-116">-DefaultProfile</span></span>
<span data-ttu-id="b61d8-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b61d8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b61d8-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b61d8-118">-DisplayName</span></span>
<span data-ttu-id="b61d8-119">Nome visualizzato del gruppo da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="b61d8-119">The display name of the group to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b61d8-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b61d8-120">-Force</span></span>
<span data-ttu-id="b61d8-121">Se specificato, non chiede conferma per l'eliminazione del gruppo.</span><span class="sxs-lookup"><span data-stu-id="b61d8-121">If specified, doesn't ask for confirmation for deleting the group.</span></span>

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

### <span data-ttu-id="b61d8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b61d8-122">-InputObject</span></span>
<span data-ttu-id="b61d8-123">Rappresentazione dell'oggetto del gruppo da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="b61d8-123">The object representation of the group to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b61d8-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b61d8-124">-ObjectId</span></span>
<span data-ttu-id="b61d8-125">ID oggetto del gruppo da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="b61d8-125">The object id of the group to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b61d8-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b61d8-126">-PassThru</span></span>
<span data-ttu-id="b61d8-127">Se si specifica questo valore, viene restituito true se il comando ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="b61d8-127">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="b61d8-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b61d8-128">-Confirm</span></span>
<span data-ttu-id="b61d8-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b61d8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b61d8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b61d8-130">-WhatIf</span></span>
<span data-ttu-id="b61d8-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b61d8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b61d8-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b61d8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b61d8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b61d8-133">CommonParameters</span></span>
<span data-ttu-id="b61d8-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b61d8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b61d8-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b61d8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b61d8-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="b61d8-136">INPUTS</span></span>

### <span data-ttu-id="b61d8-137">System.String</span><span class="sxs-lookup"><span data-stu-id="b61d8-137">System.String</span></span>

### <span data-ttu-id="b61d8-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="b61d8-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="b61d8-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b61d8-139">OUTPUTS</span></span>

### <span data-ttu-id="b61d8-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b61d8-140">System.Boolean</span></span>

## <span data-ttu-id="b61d8-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="b61d8-141">NOTES</span></span>

## <span data-ttu-id="b61d8-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b61d8-142">RELATED LINKS</span></span>
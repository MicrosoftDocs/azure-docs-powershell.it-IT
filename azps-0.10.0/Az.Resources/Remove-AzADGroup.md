---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADGroup.md
ms.openlocfilehash: 4d285471632c9c4bc952b2dcdc0e4ce5147fac12
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862457"
---
# <span data-ttu-id="db887-101">Remove-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="db887-101">Remove-AzADGroup</span></span>

## <span data-ttu-id="db887-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db887-102">SYNOPSIS</span></span>
<span data-ttu-id="db887-103">Elimina un gruppo di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="db887-103">Deletes an active directory group.</span></span>

## <span data-ttu-id="db887-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db887-104">SYNTAX</span></span>

### <span data-ttu-id="db887-105">ObjectIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="db887-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADGroup -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db887-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="db887-106">DisplayNameParameterSet</span></span>
```
Remove-AzADGroup -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db887-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db887-107">InputObjectParameterSet</span></span>
```
Remove-AzADGroup -InputObject <PSADGroup> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db887-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db887-108">DESCRIPTION</span></span>
<span data-ttu-id="db887-109">Elimina un gruppo di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="db887-109">Deletes an active directory group.</span></span>

## <span data-ttu-id="db887-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db887-110">EXAMPLES</span></span>

### <span data-ttu-id="db887-111">Esempio 1-rimuovere un gruppo per ID oggetto</span><span class="sxs-lookup"><span data-stu-id="db887-111">Example 1 - Remove a group by object id</span></span>

```
PS C:\> Remove-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="db887-112">Rimuove il gruppo con l'ID oggetto "85F89C90-780E-4AA6-9F4F-6F268D322EEE" dal tenant.</span><span class="sxs-lookup"><span data-stu-id="db887-112">Removes the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' from the tenant.</span></span>

### <span data-ttu-id="db887-113">Esempio 2-rimuovere un gruppo per piping</span><span class="sxs-lookup"><span data-stu-id="db887-113">Example 2 - Remove a group by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroup
```

<span data-ttu-id="db887-114">Ottiene il gruppo con l'ID oggetto "85F89C90-780E-4AA6-9F4F-6F268D322EEE" e le pipe da Remove-AzADGroup per rimuovere il gruppo dal tenant.</span><span class="sxs-lookup"><span data-stu-id="db887-114">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes that to Remove-AzADGroup to remove the group from the tenant.</span></span>

## <span data-ttu-id="db887-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db887-115">PARAMETERS</span></span>

### <span data-ttu-id="db887-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db887-116">-DefaultProfile</span></span>
<span data-ttu-id="db887-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db887-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db887-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="db887-118">-DisplayName</span></span>
<span data-ttu-id="db887-119">Nome visualizzato del gruppo da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="db887-119">The display name of the group to be removed.</span></span>

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

### <span data-ttu-id="db887-120">-Force</span><span class="sxs-lookup"><span data-stu-id="db887-120">-Force</span></span>
<span data-ttu-id="db887-121">Se specificato, non chiede conferma per l'eliminazione del gruppo.</span><span class="sxs-lookup"><span data-stu-id="db887-121">If specified, doesn't ask for confirmation for deleting the group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db887-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db887-122">-InputObject</span></span>
<span data-ttu-id="db887-123">Rappresentazione dell'oggetto del gruppo da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="db887-123">The object representation of the group to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db887-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="db887-124">-ObjectId</span></span>
<span data-ttu-id="db887-125">ID oggetto del gruppo da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="db887-125">The object id of the group to be removed.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db887-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db887-126">-PassThru</span></span>
<span data-ttu-id="db887-127">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="db887-127">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db887-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="db887-128">-Confirm</span></span>
<span data-ttu-id="db887-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db887-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db887-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db887-130">-WhatIf</span></span>
<span data-ttu-id="db887-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db887-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db887-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db887-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db887-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db887-133">CommonParameters</span></span>
<span data-ttu-id="db887-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db887-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db887-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db887-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db887-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db887-136">INPUTS</span></span>

### <span data-ttu-id="db887-137">System. Guid</span><span class="sxs-lookup"><span data-stu-id="db887-137">System.Guid</span></span>

### <span data-ttu-id="db887-138">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="db887-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="db887-139">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="db887-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="db887-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db887-140">OUTPUTS</span></span>

### <span data-ttu-id="db887-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="db887-141">System.Boolean</span></span>

## <span data-ttu-id="db887-142">Note</span><span class="sxs-lookup"><span data-stu-id="db887-142">NOTES</span></span>

## <span data-ttu-id="db887-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db887-143">RELATED LINKS</span></span>

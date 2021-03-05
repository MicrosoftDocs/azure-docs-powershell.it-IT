---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 9ab7607dd358e7c439539e99d44b263136f07cb4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968365"
---
# <span data-ttu-id="be60f-101">Remove-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="be60f-101">Remove-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="be60f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be60f-102">SYNOPSIS</span></span>
<span data-ttu-id="be60f-103">Elimina una configurazione di Active Directory File (ANF) di Azure NetApp.</span><span class="sxs-lookup"><span data-stu-id="be60f-103">Deletes an Azure NetApp Files (ANF) active directory configuration.</span></span>

## <span data-ttu-id="be60f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="be60f-104">SYNTAX</span></span>

### <span data-ttu-id="be60f-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="be60f-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 -ActiveDirectoryId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be60f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="be60f-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesActiveDirectory -ActiveDirectoryId <String> -AccountObject <PSNetAppFilesAccount>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be60f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="be60f-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesActiveDirectory -InputObject <PSNetAppFilesActiveDirectory> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be60f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="be60f-108">DESCRIPTION</span></span>
<span data-ttu-id="be60f-109">Il cmdlet **Remove-AzNetAppFilesActiveDirectory** elimina una configurazione di Active Directory ANF.</span><span class="sxs-lookup"><span data-stu-id="be60f-109">The **Remove-AzNetAppFilesActiveDirectory** cmdlet deletes an ANF active directory configuration.</span></span>

## <span data-ttu-id="be60f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="be60f-110">EXAMPLES</span></span>

### <span data-ttu-id="be60f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="be60f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyADName"
```

<span data-ttu-id="be60f-112">Questo comando elimina la nuova configurazione di Active Directory ANF con il nome "MyADName".</span><span class="sxs-lookup"><span data-stu-id="be60f-112">This command deletes the new ANF active directory configuration with a the name "MyADName".</span></span>

## <span data-ttu-id="be60f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be60f-113">PARAMETERS</span></span>

### <span data-ttu-id="be60f-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="be60f-114">-AccountName</span></span>
<span data-ttu-id="be60f-115">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="be60f-115">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be60f-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="be60f-116">-AccountObject</span></span>
<span data-ttu-id="be60f-117">Account per l'oggetto Active Directory</span><span class="sxs-lookup"><span data-stu-id="be60f-117">The Account for the Active Directory object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be60f-118">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="be60f-118">-ActiveDirectoryId</span></span>
<span data-ttu-id="be60f-119">ID di Active Directory ANF</span><span class="sxs-lookup"><span data-stu-id="be60f-119">The ID of the ANF active directory</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be60f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be60f-120">-DefaultProfile</span></span>
<span data-ttu-id="be60f-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="be60f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be60f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be60f-122">-InputObject</span></span>
<span data-ttu-id="be60f-123">L'oggetto Active Directory da rimuovere</span><span class="sxs-lookup"><span data-stu-id="be60f-123">The active directory object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be60f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be60f-124">-PassThru</span></span>
<span data-ttu-id="be60f-125">Verificare se Active Directory specificato è stato rimosso correttamente</span><span class="sxs-lookup"><span data-stu-id="be60f-125">Return whether the specified Active Directory  was successfully removed</span></span>

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

### <span data-ttu-id="be60f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be60f-126">-ResourceGroupName</span></span>
<span data-ttu-id="be60f-127">Gruppo di risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="be60f-127">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be60f-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be60f-128">-Confirm</span></span>
<span data-ttu-id="be60f-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be60f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be60f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be60f-130">-WhatIf</span></span>
<span data-ttu-id="be60f-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="be60f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be60f-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="be60f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be60f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be60f-133">CommonParameters</span></span>
<span data-ttu-id="be60f-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be60f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be60f-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="be60f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be60f-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="be60f-136">INPUTS</span></span>

### <span data-ttu-id="be60f-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="be60f-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="be60f-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="be60f-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="be60f-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="be60f-139">OUTPUTS</span></span>

### <span data-ttu-id="be60f-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="be60f-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="be60f-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="be60f-141">NOTES</span></span>

## <span data-ttu-id="be60f-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="be60f-142">RELATED LINKS</span></span>

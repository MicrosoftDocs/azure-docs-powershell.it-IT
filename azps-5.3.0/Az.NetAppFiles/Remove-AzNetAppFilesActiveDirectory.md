---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 7fcf1f749816872fb7407fedaea10d06f3385441
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486799"
---
# <span data-ttu-id="8ed48-101">Remove-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="8ed48-101">Remove-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="8ed48-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8ed48-102">SYNOPSIS</span></span>
<span data-ttu-id="8ed48-103">Elimina una configurazione di Active Directory di Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="8ed48-103">Deletes an Azure NetApp Files (ANF) active directory configuration.</span></span>

## <span data-ttu-id="8ed48-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8ed48-104">SYNTAX</span></span>

### <span data-ttu-id="8ed48-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8ed48-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 -ActiveDirectoryId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ed48-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ed48-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesActiveDirectory -ActiveDirectoryId <String> -AccountObject <PSNetAppFilesAccount>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ed48-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ed48-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesActiveDirectory -InputObject <PSNetAppFilesActiveDirectory> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ed48-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ed48-108">DESCRIPTION</span></span>
<span data-ttu-id="8ed48-109">Il cmdlet **Remove-AzNetAppFilesActiveDirectory** Elimina una configurazione di Active Directory di ANF.</span><span class="sxs-lookup"><span data-stu-id="8ed48-109">The **Remove-AzNetAppFilesActiveDirectory** cmdlet deletes an ANF active directory configuration.</span></span>

## <span data-ttu-id="8ed48-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8ed48-110">EXAMPLES</span></span>

### <span data-ttu-id="8ed48-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8ed48-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyADName"
```

<span data-ttu-id="8ed48-112">Questo comando Elimina la nuova configurazione di Active Directory di ANF con il nome "MyADName".</span><span class="sxs-lookup"><span data-stu-id="8ed48-112">This command deletes the new ANF active directory configuration with a the name "MyADName".</span></span>

## <span data-ttu-id="8ed48-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8ed48-113">PARAMETERS</span></span>

### <span data-ttu-id="8ed48-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8ed48-114">-AccountName</span></span>
<span data-ttu-id="8ed48-115">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="8ed48-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="8ed48-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="8ed48-116">-AccountObject</span></span>
<span data-ttu-id="8ed48-117">Account per l'oggetto Active Directory</span><span class="sxs-lookup"><span data-stu-id="8ed48-117">The Account for the Active Directory object</span></span>

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

### <span data-ttu-id="8ed48-118">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="8ed48-118">-ActiveDirectoryId</span></span>
<span data-ttu-id="8ed48-119">ID della ANF Active Directory</span><span class="sxs-lookup"><span data-stu-id="8ed48-119">The ID of the ANF active directory</span></span>

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

### <span data-ttu-id="8ed48-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ed48-120">-DefaultProfile</span></span>
<span data-ttu-id="8ed48-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8ed48-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ed48-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ed48-122">-InputObject</span></span>
<span data-ttu-id="8ed48-123">Oggetto Active Directory da rimuovere</span><span class="sxs-lookup"><span data-stu-id="8ed48-123">The active directory object to remove</span></span>

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

### <span data-ttu-id="8ed48-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ed48-124">-PassThru</span></span>
<span data-ttu-id="8ed48-125">Restituisce se l'Active Directory specificata è stata rimossa correttamente</span><span class="sxs-lookup"><span data-stu-id="8ed48-125">Return whether the specified Active Directory  was successfully removed</span></span>

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

### <span data-ttu-id="8ed48-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ed48-126">-ResourceGroupName</span></span>
<span data-ttu-id="8ed48-127">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="8ed48-127">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="8ed48-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8ed48-128">-Confirm</span></span>
<span data-ttu-id="8ed48-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ed48-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ed48-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ed48-130">-WhatIf</span></span>
<span data-ttu-id="8ed48-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8ed48-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ed48-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8ed48-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ed48-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ed48-133">CommonParameters</span></span>
<span data-ttu-id="8ed48-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ed48-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ed48-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ed48-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ed48-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8ed48-136">INPUTS</span></span>

### <span data-ttu-id="8ed48-137">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="8ed48-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="8ed48-138">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="8ed48-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="8ed48-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8ed48-139">OUTPUTS</span></span>

### <span data-ttu-id="8ed48-140">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="8ed48-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="8ed48-141">Note</span><span class="sxs-lookup"><span data-stu-id="8ed48-141">NOTES</span></span>

## <span data-ttu-id="8ed48-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8ed48-142">RELATED LINKS</span></span>

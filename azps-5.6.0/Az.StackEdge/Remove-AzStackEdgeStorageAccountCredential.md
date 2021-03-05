---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/remove-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: b5abdb8e539eb60df2ec231c6584c792fa4462e9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005102"
---
# <span data-ttu-id="8d91f-101">Remove-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="8d91f-101">Remove-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="8d91f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d91f-102">SYNOPSIS</span></span>
<span data-ttu-id="8d91f-103">Rimuove le credenziali di un account di archiviazione per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d91f-103">Removes a storage account credential for a device.</span></span>

## <span data-ttu-id="8d91f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8d91f-104">SYNTAX</span></span>

### <span data-ttu-id="8d91f-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8d91f-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d91f-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d91f-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d91f-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d91f-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-InputObject] <PSStackEdgeStorageAccountCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d91f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8d91f-108">DESCRIPTION</span></span>
<span data-ttu-id="8d91f-109">Il cmdlet **Remove-AzStackEdgeStorageAccountCredential** rimuove le credenziali dell'account di archiviazione per un dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="8d91f-109">The **Remove-AzStackEdgeStorageAccountCredential** cmdlet removes the storage account credential for a Stack Edge device.</span></span>

## <span data-ttu-id="8d91f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8d91f-110">EXAMPLES</span></span>

### <span data-ttu-id="8d91f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8d91f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccountCredential ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAccountCredentialName
```

## <span data-ttu-id="8d91f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d91f-112">PARAMETERS</span></span>

### <span data-ttu-id="8d91f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d91f-113">-AsJob</span></span>
<span data-ttu-id="8d91f-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8d91f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8d91f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d91f-115">-DefaultProfile</span></span>
<span data-ttu-id="8d91f-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8d91f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d91f-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8d91f-117">-DeviceName</span></span>
<span data-ttu-id="8d91f-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="8d91f-118">Device Name</span></span>

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

### <span data-ttu-id="8d91f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d91f-119">-InputObject</span></span>
<span data-ttu-id="8d91f-120">Oggetto input</span><span class="sxs-lookup"><span data-stu-id="8d91f-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d91f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8d91f-121">-Name</span></span>
<span data-ttu-id="8d91f-122">Nome dell'account di archiviazione da usare</span><span class="sxs-lookup"><span data-stu-id="8d91f-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d91f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d91f-123">-PassThru</span></span>
<span data-ttu-id="8d91f-124">restituisce true se ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="8d91f-124">returns true if successful</span></span>

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

### <span data-ttu-id="8d91f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d91f-125">-ResourceGroupName</span></span>
<span data-ttu-id="8d91f-126">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="8d91f-126">Resource Group Name</span></span>

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

### <span data-ttu-id="8d91f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d91f-127">-ResourceId</span></span>
<span data-ttu-id="8d91f-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d91f-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="8d91f-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d91f-129">-Confirm</span></span>
<span data-ttu-id="8d91f-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d91f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d91f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d91f-131">-WhatIf</span></span>
<span data-ttu-id="8d91f-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8d91f-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8d91f-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8d91f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d91f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d91f-134">CommonParameters</span></span>
<span data-ttu-id="8d91f-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d91f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d91f-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8d91f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d91f-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="8d91f-137">INPUTS</span></span>

### <span data-ttu-id="8d91f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="8d91f-138">System.String</span></span>

### <span data-ttu-id="8d91f-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="8d91f-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="8d91f-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8d91f-140">OUTPUTS</span></span>

### <span data-ttu-id="8d91f-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8d91f-141">System.Boolean</span></span>

## <span data-ttu-id="8d91f-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="8d91f-142">NOTES</span></span>

## <span data-ttu-id="8d91f-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8d91f-143">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 00cfc136465cc250d068344158d66f98dc6e0704
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298693"
---
# <span data-ttu-id="7a74b-101">Remove-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="7a74b-101">Remove-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="7a74b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7a74b-102">SYNOPSIS</span></span>
<span data-ttu-id="7a74b-103">Rimuove una credenziale dell'account di archiviazione per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7a74b-103">Removes a storage account credential for a device.</span></span>

## <span data-ttu-id="7a74b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7a74b-104">SYNTAX</span></span>

### <span data-ttu-id="7a74b-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7a74b-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7a74b-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a74b-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccountCredential [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a74b-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a74b-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccountCredential [-InputObject] <PSDataBoxEdgeStorageAccountCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a74b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a74b-108">DESCRIPTION</span></span>
<span data-ttu-id="7a74b-109">Il cmdlet **Remove-AzDataBoxEdgeStorageAccountCredential** rimuove le credenziali dell'account di archiviazione per un dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="7a74b-109">The **Remove-AzDataBoxEdgeStorageAccountCredential** cmdlet removes the storage account credential for a Data Box Edge device.</span></span>

## <span data-ttu-id="7a74b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7a74b-110">EXAMPLES</span></span>

### <span data-ttu-id="7a74b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7a74b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageAccountCredential ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAccountCredentialName
```

## <span data-ttu-id="7a74b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7a74b-112">PARAMETERS</span></span>

### <span data-ttu-id="7a74b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a74b-113">-AsJob</span></span>
<span data-ttu-id="7a74b-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7a74b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a74b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a74b-115">-DefaultProfile</span></span>
<span data-ttu-id="7a74b-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7a74b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a74b-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="7a74b-117">-DeviceName</span></span>
<span data-ttu-id="7a74b-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="7a74b-118">Device Name</span></span>

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

### <span data-ttu-id="7a74b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a74b-119">-InputObject</span></span>
<span data-ttu-id="7a74b-120">Oggetto di input</span><span class="sxs-lookup"><span data-stu-id="7a74b-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a74b-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="7a74b-121">-Name</span></span>
<span data-ttu-id="7a74b-122">Nome dell'account di archiviazione da usare</span><span class="sxs-lookup"><span data-stu-id="7a74b-122">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="7a74b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a74b-123">-PassThru</span></span>
<span data-ttu-id="7a74b-124">Restituisce vero in caso di esito positivo</span><span class="sxs-lookup"><span data-stu-id="7a74b-124">returns true if successful</span></span>

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

### <span data-ttu-id="7a74b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a74b-125">-ResourceGroupName</span></span>
<span data-ttu-id="7a74b-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="7a74b-126">Resource Group Name</span></span>

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

### <span data-ttu-id="7a74b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a74b-127">-ResourceId</span></span>
<span data-ttu-id="7a74b-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a74b-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="7a74b-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7a74b-129">-Confirm</span></span>
<span data-ttu-id="7a74b-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a74b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a74b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a74b-131">-WhatIf</span></span>
<span data-ttu-id="7a74b-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a74b-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7a74b-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a74b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a74b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a74b-134">CommonParameters</span></span>
<span data-ttu-id="7a74b-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a74b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a74b-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a74b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a74b-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7a74b-137">INPUTS</span></span>

### <span data-ttu-id="7a74b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="7a74b-138">System.String</span></span>

### <span data-ttu-id="7a74b-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="7a74b-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="7a74b-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7a74b-140">OUTPUTS</span></span>

### <span data-ttu-id="7a74b-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7a74b-141">System.Boolean</span></span>

## <span data-ttu-id="7a74b-142">Note</span><span class="sxs-lookup"><span data-stu-id="7a74b-142">NOTES</span></span>

## <span data-ttu-id="7a74b-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7a74b-143">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: 1a55a8c08182ae4a32e27bec74e4a5870aae95fa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374373"
---
# <span data-ttu-id="7b0d2-101">Remove-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="7b0d2-101">Remove-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="7b0d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7b0d2-102">SYNOPSIS</span></span>
<span data-ttu-id="7b0d2-103">Rimuove una credenziale dell'account di archiviazione per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7b0d2-103">Removes a storage account credential for a device.</span></span>

## <span data-ttu-id="7b0d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b0d2-104">SYNTAX</span></span>

### <span data-ttu-id="7b0d2-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7b0d2-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7b0d2-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b0d2-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b0d2-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b0d2-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-InputObject] <PSStackEdgeStorageAccountCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b0d2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b0d2-108">DESCRIPTION</span></span>
<span data-ttu-id="7b0d2-109">Il cmdlet **Remove-AzStackEdgeStorageAccountCredential** rimuove le credenziali dell'account di archiviazione per un dispositivo a bordo dello stack.</span><span class="sxs-lookup"><span data-stu-id="7b0d2-109">The **Remove-AzStackEdgeStorageAccountCredential** cmdlet removes the storage account credential for a Stack Edge device.</span></span>

## <span data-ttu-id="7b0d2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b0d2-110">EXAMPLES</span></span>

### <span data-ttu-id="7b0d2-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7b0d2-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccountCredential ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAccountCredentialName
```

## <span data-ttu-id="7b0d2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7b0d2-112">PARAMETERS</span></span>

### <span data-ttu-id="7b0d2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b0d2-113">-AsJob</span></span>
<span data-ttu-id="7b0d2-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7b0d2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7b0d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b0d2-115">-DefaultProfile</span></span>
<span data-ttu-id="7b0d2-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7b0d2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b0d2-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="7b0d2-117">-DeviceName</span></span>
<span data-ttu-id="7b0d2-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="7b0d2-118">Device Name</span></span>

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

### <span data-ttu-id="7b0d2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b0d2-119">-InputObject</span></span>
<span data-ttu-id="7b0d2-120">Oggetto di input</span><span class="sxs-lookup"><span data-stu-id="7b0d2-120">Input Object</span></span>

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

### <span data-ttu-id="7b0d2-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="7b0d2-121">-Name</span></span>
<span data-ttu-id="7b0d2-122">Nome dell'account di archiviazione da usare</span><span class="sxs-lookup"><span data-stu-id="7b0d2-122">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="7b0d2-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b0d2-123">-PassThru</span></span>
<span data-ttu-id="7b0d2-124">Restituisce vero in caso di esito positivo</span><span class="sxs-lookup"><span data-stu-id="7b0d2-124">returns true if successful</span></span>

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

### <span data-ttu-id="7b0d2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b0d2-125">-ResourceGroupName</span></span>
<span data-ttu-id="7b0d2-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="7b0d2-126">Resource Group Name</span></span>

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

### <span data-ttu-id="7b0d2-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b0d2-127">-ResourceId</span></span>
<span data-ttu-id="7b0d2-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b0d2-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="7b0d2-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7b0d2-129">-Confirm</span></span>
<span data-ttu-id="7b0d2-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b0d2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b0d2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b0d2-131">-WhatIf</span></span>
<span data-ttu-id="7b0d2-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b0d2-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b0d2-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b0d2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b0d2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b0d2-134">CommonParameters</span></span>
<span data-ttu-id="7b0d2-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b0d2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b0d2-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b0d2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b0d2-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7b0d2-137">INPUTS</span></span>

### <span data-ttu-id="7b0d2-138">System. String</span><span class="sxs-lookup"><span data-stu-id="7b0d2-138">System.String</span></span>

### <span data-ttu-id="7b0d2-139">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="7b0d2-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="7b0d2-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b0d2-140">OUTPUTS</span></span>

### <span data-ttu-id="7b0d2-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7b0d2-141">System.Boolean</span></span>

## <span data-ttu-id="7b0d2-142">Note</span><span class="sxs-lookup"><span data-stu-id="7b0d2-142">NOTES</span></span>

## <span data-ttu-id="7b0d2-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b0d2-143">RELATED LINKS</span></span>

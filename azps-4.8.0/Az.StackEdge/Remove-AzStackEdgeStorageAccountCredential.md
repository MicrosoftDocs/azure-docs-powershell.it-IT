---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: 1a55a8c08182ae4a32e27bec74e4a5870aae95fa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191169"
---
# <span data-ttu-id="dfb40-101">Remove-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="dfb40-101">Remove-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="dfb40-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dfb40-102">SYNOPSIS</span></span>
<span data-ttu-id="dfb40-103">Rimuove una credenziale dell'account di archiviazione per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dfb40-103">Removes a storage account credential for a device.</span></span>

## <span data-ttu-id="dfb40-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dfb40-104">SYNTAX</span></span>

### <span data-ttu-id="dfb40-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dfb40-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dfb40-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dfb40-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfb40-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dfb40-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-InputObject] <PSStackEdgeStorageAccountCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfb40-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dfb40-108">DESCRIPTION</span></span>
<span data-ttu-id="dfb40-109">Il cmdlet **Remove-AzStackEdgeStorageAccountCredential** rimuove le credenziali dell'account di archiviazione per un dispositivo a bordo dello stack.</span><span class="sxs-lookup"><span data-stu-id="dfb40-109">The **Remove-AzStackEdgeStorageAccountCredential** cmdlet removes the storage account credential for a Stack Edge device.</span></span>

## <span data-ttu-id="dfb40-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dfb40-110">EXAMPLES</span></span>

### <span data-ttu-id="dfb40-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dfb40-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccountCredential ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAccountCredentialName
```

## <span data-ttu-id="dfb40-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dfb40-112">PARAMETERS</span></span>

### <span data-ttu-id="dfb40-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dfb40-113">-AsJob</span></span>
<span data-ttu-id="dfb40-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="dfb40-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dfb40-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfb40-115">-DefaultProfile</span></span>
<span data-ttu-id="dfb40-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dfb40-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfb40-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="dfb40-117">-DeviceName</span></span>
<span data-ttu-id="dfb40-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="dfb40-118">Device Name</span></span>

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

### <span data-ttu-id="dfb40-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dfb40-119">-InputObject</span></span>
<span data-ttu-id="dfb40-120">Oggetto di input</span><span class="sxs-lookup"><span data-stu-id="dfb40-120">Input Object</span></span>

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

### <span data-ttu-id="dfb40-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="dfb40-121">-Name</span></span>
<span data-ttu-id="dfb40-122">Nome dell'account di archiviazione da usare</span><span class="sxs-lookup"><span data-stu-id="dfb40-122">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="dfb40-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dfb40-123">-PassThru</span></span>
<span data-ttu-id="dfb40-124">Restituisce vero in caso di esito positivo</span><span class="sxs-lookup"><span data-stu-id="dfb40-124">returns true if successful</span></span>

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

### <span data-ttu-id="dfb40-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfb40-125">-ResourceGroupName</span></span>
<span data-ttu-id="dfb40-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="dfb40-126">Resource Group Name</span></span>

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

### <span data-ttu-id="dfb40-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dfb40-127">-ResourceId</span></span>
<span data-ttu-id="dfb40-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="dfb40-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="dfb40-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dfb40-129">-Confirm</span></span>
<span data-ttu-id="dfb40-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfb40-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfb40-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfb40-131">-WhatIf</span></span>
<span data-ttu-id="dfb40-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dfb40-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dfb40-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dfb40-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfb40-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfb40-134">CommonParameters</span></span>
<span data-ttu-id="dfb40-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfb40-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfb40-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dfb40-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfb40-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dfb40-137">INPUTS</span></span>

### <span data-ttu-id="dfb40-138">System. String</span><span class="sxs-lookup"><span data-stu-id="dfb40-138">System.String</span></span>

### <span data-ttu-id="dfb40-139">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="dfb40-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="dfb40-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dfb40-140">OUTPUTS</span></span>

### <span data-ttu-id="dfb40-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dfb40-141">System.Boolean</span></span>

## <span data-ttu-id="dfb40-142">Note</span><span class="sxs-lookup"><span data-stu-id="dfb40-142">NOTES</span></span>

## <span data-ttu-id="dfb40-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dfb40-143">RELATED LINKS</span></span>

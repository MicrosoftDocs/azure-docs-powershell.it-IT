---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
ms.openlocfilehash: d4b815e0caa85bee26086f475f86e1757b690fbd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191170"
---
# <span data-ttu-id="f264d-101">Remove-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f264d-101">Remove-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="f264d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f264d-102">SYNOPSIS</span></span>
<span data-ttu-id="f264d-103">Consente di rimuovere l'account di archiviazione perimetrale per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f264d-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="f264d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f264d-104">SYNTAX</span></span>

### <span data-ttu-id="f264d-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f264d-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f264d-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f264d-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f264d-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f264d-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-InputObject] <PSStackEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f264d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f264d-108">DESCRIPTION</span></span>
<span data-ttu-id="f264d-109">Il cmdlet **Remove-AzStackEdgeStorageAccount** consente di rimuovere un account di archiviazione Edge associato per un dispositivo di bordo dello stack.</span><span class="sxs-lookup"><span data-stu-id="f264d-109">The **Remove-AzStackEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Stack Edge device.</span></span> <span data-ttu-id="f264d-110">È possibile specificare il nome dell'account di archiviazione Edge da rimuovere come parametro nel cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f264d-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="f264d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f264d-111">EXAMPLES</span></span>

### <span data-ttu-id="f264d-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f264d-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="f264d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f264d-113">PARAMETERS</span></span>

### <span data-ttu-id="f264d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f264d-114">-AsJob</span></span>
<span data-ttu-id="f264d-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f264d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f264d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f264d-116">-DefaultProfile</span></span>
<span data-ttu-id="f264d-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f264d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f264d-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f264d-118">-DeviceName</span></span>
<span data-ttu-id="f264d-119">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="f264d-119">Device Name</span></span>

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

### <span data-ttu-id="f264d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f264d-120">-InputObject</span></span>
<span data-ttu-id="f264d-121">Oggetto di input</span><span class="sxs-lookup"><span data-stu-id="f264d-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeStorageAccount

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f264d-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="f264d-122">-Name</span></span>
<span data-ttu-id="f264d-123">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="f264d-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeStorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f264d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f264d-124">-PassThru</span></span>
<span data-ttu-id="f264d-125">Restituisce vero in caso di esito positivo</span><span class="sxs-lookup"><span data-stu-id="f264d-125">returns true if successful</span></span>

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

### <span data-ttu-id="f264d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f264d-126">-ResourceGroupName</span></span>
<span data-ttu-id="f264d-127">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="f264d-127">Resource Group Name</span></span>

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

### <span data-ttu-id="f264d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f264d-128">-ResourceId</span></span>
<span data-ttu-id="f264d-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="f264d-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="f264d-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f264d-130">-Confirm</span></span>
<span data-ttu-id="f264d-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f264d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f264d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f264d-132">-WhatIf</span></span>
<span data-ttu-id="f264d-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f264d-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f264d-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f264d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f264d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f264d-135">CommonParameters</span></span>
<span data-ttu-id="f264d-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f264d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f264d-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f264d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f264d-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f264d-138">INPUTS</span></span>

### <span data-ttu-id="f264d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f264d-139">System.String</span></span>

### <span data-ttu-id="f264d-140">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f264d-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="f264d-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f264d-141">OUTPUTS</span></span>

### <span data-ttu-id="f264d-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f264d-142">System.Boolean</span></span>

## <span data-ttu-id="f264d-143">Note</span><span class="sxs-lookup"><span data-stu-id="f264d-143">NOTES</span></span>

## <span data-ttu-id="f264d-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f264d-144">RELATED LINKS</span></span>

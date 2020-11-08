---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageContainer.md
ms.openlocfilehash: c1e76da1fc01ea1698c56e40fd3bd46f6378ea07
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191164"
---
# <span data-ttu-id="0f3e5-101">Remove-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0f3e5-101">Remove-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="0f3e5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0f3e5-102">SYNOPSIS</span></span>
<span data-ttu-id="0f3e5-103">Rimuove un contenitore di archiviazione per l'account di archiviazione perimetrale in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-103">Removes a storage container for the Edge Storage account on a device.</span></span>

## <span data-ttu-id="0f3e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f3e5-104">SYNTAX</span></span>

### <span data-ttu-id="0f3e5-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0f3e5-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f3e5-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f3e5-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageContainer -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f3e5-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f3e5-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageContainer -InputObject <PSStackEdgeStorageContainer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f3e5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f3e5-108">DESCRIPTION</span></span>
<span data-ttu-id="0f3e5-109">Il cmdlet **Remove-AzStackEdgeStorageContainer** rimuove un contenitore di archiviazione associato per l'account di archiviazione perimetrale in un dispositivo di bordo dello stack.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-109">The **Remove-AzStackEdgeStorageContainer** cmdlet removes an associated storage container for the Edge Storage account on a Stack Edge device.</span></span> <span data-ttu-id="0f3e5-110">Puoi specificare il nome del contenitore di archiviazione da rimuovere come parametro.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-110">You can specify the name of the storage container to be removed as a parameter.</span></span>

## <span data-ttu-id="0f3e5-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f3e5-111">EXAMPLES</span></span>

### <span data-ttu-id="0f3e5-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0f3e5-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccountname -Name container1
```

## <span data-ttu-id="0f3e5-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0f3e5-113">PARAMETERS</span></span>

### <span data-ttu-id="0f3e5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f3e5-114">-AsJob</span></span>
<span data-ttu-id="0f3e5-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="0f3e5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f3e5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f3e5-116">-DefaultProfile</span></span>
<span data-ttu-id="0f3e5-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f3e5-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="0f3e5-118">-DeviceName</span></span>
<span data-ttu-id="0f3e5-119">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="0f3e5-119">Device Name</span></span>

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

### <span data-ttu-id="0f3e5-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0f3e5-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="0f3e5-121">Fornisci il nome di EdgeStorageAccount esistente</span><span class="sxs-lookup"><span data-stu-id="0f3e5-121">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f3e5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f3e5-122">-InputObject</span></span>
<span data-ttu-id="0f3e5-123">Oggetto di input</span><span class="sxs-lookup"><span data-stu-id="0f3e5-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeStorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f3e5-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="0f3e5-124">-Name</span></span>
<span data-ttu-id="0f3e5-125">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="0f3e5-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f3e5-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f3e5-126">-PassThru</span></span>
<span data-ttu-id="0f3e5-127">Restituisce vero in caso di esito positivo</span><span class="sxs-lookup"><span data-stu-id="0f3e5-127">returns true if successful</span></span>

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

### <span data-ttu-id="0f3e5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f3e5-128">-ResourceGroupName</span></span>
<span data-ttu-id="0f3e5-129">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="0f3e5-129">Resource Group Name</span></span>

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

### <span data-ttu-id="0f3e5-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f3e5-130">-ResourceId</span></span>
<span data-ttu-id="0f3e5-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f3e5-131">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f3e5-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0f3e5-132">-Confirm</span></span>
<span data-ttu-id="0f3e5-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f3e5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f3e5-134">-WhatIf</span></span>
<span data-ttu-id="0f3e5-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0f3e5-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f3e5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f3e5-137">CommonParameters</span></span>
<span data-ttu-id="0f3e5-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f3e5-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f3e5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f3e5-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0f3e5-140">INPUTS</span></span>

### <span data-ttu-id="0f3e5-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0f3e5-141">System.String</span></span>

### <span data-ttu-id="0f3e5-142">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0f3e5-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="0f3e5-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f3e5-143">OUTPUTS</span></span>

### <span data-ttu-id="0f3e5-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0f3e5-144">System.Boolean</span></span>

## <span data-ttu-id="0f3e5-145">Note</span><span class="sxs-lookup"><span data-stu-id="0f3e5-145">NOTES</span></span>

## <span data-ttu-id="0f3e5-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f3e5-146">RELATED LINKS</span></span>

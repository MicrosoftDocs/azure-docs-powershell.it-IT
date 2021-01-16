---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageContainer.md
ms.openlocfilehash: c1e76da1fc01ea1698c56e40fd3bd46f6378ea07
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350020"
---
# <span data-ttu-id="d9e0e-101">Remove-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d9e0e-101">Remove-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="d9e0e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d9e0e-102">SYNOPSIS</span></span>
<span data-ttu-id="d9e0e-103">Rimuove un contenitore di archiviazione per l'account di archiviazione perimetrale in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d9e0e-103">Removes a storage container for the Edge Storage account on a device.</span></span>

## <span data-ttu-id="d9e0e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9e0e-104">SYNTAX</span></span>

### <span data-ttu-id="d9e0e-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d9e0e-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9e0e-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9e0e-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageContainer -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9e0e-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9e0e-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageContainer -InputObject <PSStackEdgeStorageContainer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9e0e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9e0e-108">DESCRIPTION</span></span>
<span data-ttu-id="d9e0e-109">Il cmdlet **Remove-AzStackEdgeStorageContainer** rimuove un contenitore di archiviazione associato per l'account di archiviazione perimetrale in un dispositivo di bordo dello stack.</span><span class="sxs-lookup"><span data-stu-id="d9e0e-109">The **Remove-AzStackEdgeStorageContainer** cmdlet removes an associated storage container for the Edge Storage account on a Stack Edge device.</span></span> <span data-ttu-id="d9e0e-110">Puoi specificare il nome del contenitore di archiviazione da rimuovere come parametro.</span><span class="sxs-lookup"><span data-stu-id="d9e0e-110">You can specify the name of the storage container to be removed as a parameter.</span></span>

## <span data-ttu-id="d9e0e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9e0e-111">EXAMPLES</span></span>

### <span data-ttu-id="d9e0e-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d9e0e-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccountname -Name container1
```

## <span data-ttu-id="d9e0e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d9e0e-113">PARAMETERS</span></span>

### <span data-ttu-id="d9e0e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9e0e-114">-AsJob</span></span>
<span data-ttu-id="d9e0e-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d9e0e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d9e0e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9e0e-116">-DefaultProfile</span></span>
<span data-ttu-id="d9e0e-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d9e0e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9e0e-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d9e0e-118">-DeviceName</span></span>
<span data-ttu-id="d9e0e-119">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="d9e0e-119">Device Name</span></span>

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

### <span data-ttu-id="d9e0e-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d9e0e-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="d9e0e-121">Fornisci il nome di EdgeStorageAccount esistente</span><span class="sxs-lookup"><span data-stu-id="d9e0e-121">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="d9e0e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9e0e-122">-InputObject</span></span>
<span data-ttu-id="d9e0e-123">Oggetto di input</span><span class="sxs-lookup"><span data-stu-id="d9e0e-123">Input Object</span></span>

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

### <span data-ttu-id="d9e0e-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="d9e0e-124">-Name</span></span>
<span data-ttu-id="d9e0e-125">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="d9e0e-125">Resource Name</span></span>

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

### <span data-ttu-id="d9e0e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9e0e-126">-PassThru</span></span>
<span data-ttu-id="d9e0e-127">Restituisce vero in caso di esito positivo</span><span class="sxs-lookup"><span data-stu-id="d9e0e-127">returns true if successful</span></span>

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

### <span data-ttu-id="d9e0e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9e0e-128">-ResourceGroupName</span></span>
<span data-ttu-id="d9e0e-129">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="d9e0e-129">Resource Group Name</span></span>

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

### <span data-ttu-id="d9e0e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9e0e-130">-ResourceId</span></span>
<span data-ttu-id="d9e0e-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9e0e-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="d9e0e-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d9e0e-132">-Confirm</span></span>
<span data-ttu-id="d9e0e-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9e0e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9e0e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9e0e-134">-WhatIf</span></span>
<span data-ttu-id="d9e0e-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d9e0e-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d9e0e-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d9e0e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9e0e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9e0e-137">CommonParameters</span></span>
<span data-ttu-id="d9e0e-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9e0e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9e0e-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9e0e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9e0e-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d9e0e-140">INPUTS</span></span>

### <span data-ttu-id="d9e0e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d9e0e-141">System.String</span></span>

### <span data-ttu-id="d9e0e-142">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d9e0e-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="d9e0e-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9e0e-143">OUTPUTS</span></span>

### <span data-ttu-id="d9e0e-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d9e0e-144">System.Boolean</span></span>

## <span data-ttu-id="d9e0e-145">Note</span><span class="sxs-lookup"><span data-stu-id="d9e0e-145">NOTES</span></span>

## <span data-ttu-id="d9e0e-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9e0e-146">RELATED LINKS</span></span>

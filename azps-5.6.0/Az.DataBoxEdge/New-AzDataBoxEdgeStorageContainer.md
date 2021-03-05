---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 22f8d81ca68c0136802500876102fa53f8ea7a9b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978574"
---
# <span data-ttu-id="417f6-101">New-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="417f6-101">New-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="417f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="417f6-102">SYNOPSIS</span></span>
<span data-ttu-id="417f6-103">Crea un nuovo contenitore di archiviazione nell'account di archiviazione Microsoft Edge nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="417f6-103">Creates a new storage container in the Edge Storage account on the device.</span></span>

## <span data-ttu-id="417f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="417f6-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-DataFormat <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="417f6-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="417f6-105">DESCRIPTION</span></span>
<span data-ttu-id="417f6-106">Il cmdlet **New-AzDataBoxEdgeStorageContainer crea** un nuovo contenitore di archiviazione nell'account di archiviazione Edge in un dispositivo Microsoft Edge della casella di dati.</span><span class="sxs-lookup"><span data-stu-id="417f6-106">The **New-AzDataBoxEdgeStorageContainer** cmdlet creates a new storage container in the Edge Storage account on a Data Box Edge device.</span></span>

## <span data-ttu-id="417f6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="417f6-107">EXAMPLES</span></span>

### <span data-ttu-id="417f6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="417f6-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name edgecontainer1 -DataFormat BlockBlob
Name       DataFormat EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ---------------------- ---------- -----------------
container1 BlockBlob  edgestorageaccount1    db-edge    resourceGroupName
```

## <span data-ttu-id="417f6-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="417f6-109">PARAMETERS</span></span>

### <span data-ttu-id="417f6-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="417f6-110">-AsJob</span></span>
<span data-ttu-id="417f6-111">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="417f6-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="417f6-112">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="417f6-112">-DataFormat</span></span>
<span data-ttu-id="417f6-113">Impostare il formato dati ad esempio PageBlob, BLOBBlob</span><span class="sxs-lookup"><span data-stu-id="417f6-113">Set Data Format ex: PageBlob, BlobBlob</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="417f6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="417f6-114">-DefaultProfile</span></span>
<span data-ttu-id="417f6-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="417f6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="417f6-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="417f6-116">-DeviceName</span></span>
<span data-ttu-id="417f6-117">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="417f6-117">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="417f6-118">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="417f6-118">-EdgeStorageAccountName</span></span>
<span data-ttu-id="417f6-119">Fornisci il nome dell'account EdgeStorageAccount esistente</span><span class="sxs-lookup"><span data-stu-id="417f6-119">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="417f6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="417f6-120">-Name</span></span>
<span data-ttu-id="417f6-121">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="417f6-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="417f6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="417f6-122">-ResourceGroupName</span></span>
<span data-ttu-id="417f6-123">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="417f6-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="417f6-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="417f6-124">-Confirm</span></span>
<span data-ttu-id="417f6-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="417f6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="417f6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="417f6-126">-WhatIf</span></span>
<span data-ttu-id="417f6-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="417f6-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="417f6-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="417f6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="417f6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="417f6-129">CommonParameters</span></span>
<span data-ttu-id="417f6-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="417f6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="417f6-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="417f6-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="417f6-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="417f6-132">INPUTS</span></span>

### <span data-ttu-id="417f6-133">System.String</span><span class="sxs-lookup"><span data-stu-id="417f6-133">System.String</span></span>

## <span data-ttu-id="417f6-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="417f6-134">OUTPUTS</span></span>

### <span data-ttu-id="417f6-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="417f6-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="417f6-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="417f6-136">NOTES</span></span>

## <span data-ttu-id="417f6-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="417f6-137">RELATED LINKS</span></span>

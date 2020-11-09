---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 3561c77e79f0ee1be82b8f180fdf1b73879dc084
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298741"
---
# <span data-ttu-id="7844b-101">New-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7844b-101">New-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="7844b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7844b-102">SYNOPSIS</span></span>
<span data-ttu-id="7844b-103">Crea un nuovo contenitore di archiviazione nell'account di archiviazione perimetrale nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7844b-103">Creates a new storage container in the Edge Storage account on the device.</span></span>

## <span data-ttu-id="7844b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7844b-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-DataFormat <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7844b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7844b-105">DESCRIPTION</span></span>
<span data-ttu-id="7844b-106">Il cmdlet **New-AzDataBoxEdgeStorageContainer** crea un nuovo contenitore di archiviazione nell'account di archiviazione Edge in un dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="7844b-106">The **New-AzDataBoxEdgeStorageContainer** cmdlet creates a new storage container in the Edge Storage account on a Data Box Edge device.</span></span>

## <span data-ttu-id="7844b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7844b-107">EXAMPLES</span></span>

### <span data-ttu-id="7844b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7844b-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name edgecontainer1 -DataFormat BlockBlob
Name       DataFormat EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ---------------------- ---------- -----------------
container1 BlockBlob  edgestorageaccount1    db-edge    resourceGroupName
```

## <span data-ttu-id="7844b-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7844b-109">PARAMETERS</span></span>

### <span data-ttu-id="7844b-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7844b-110">-AsJob</span></span>
<span data-ttu-id="7844b-111">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7844b-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7844b-112">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="7844b-112">-DataFormat</span></span>
<span data-ttu-id="7844b-113">Impostare il formato dati ex: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="7844b-113">Set Data Format ex: PageBlob, BlobBlob</span></span>

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

### <span data-ttu-id="7844b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7844b-114">-DefaultProfile</span></span>
<span data-ttu-id="7844b-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7844b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7844b-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="7844b-116">-DeviceName</span></span>
<span data-ttu-id="7844b-117">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="7844b-117">Device Name</span></span>

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

### <span data-ttu-id="7844b-118">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7844b-118">-EdgeStorageAccountName</span></span>
<span data-ttu-id="7844b-119">Fornisci il nome di EdgeStorageAccount esistente</span><span class="sxs-lookup"><span data-stu-id="7844b-119">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="7844b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="7844b-120">-Name</span></span>
<span data-ttu-id="7844b-121">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="7844b-121">Resource Name</span></span>

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

### <span data-ttu-id="7844b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7844b-122">-ResourceGroupName</span></span>
<span data-ttu-id="7844b-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="7844b-123">Resource Group Name</span></span>

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

### <span data-ttu-id="7844b-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7844b-124">-Confirm</span></span>
<span data-ttu-id="7844b-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7844b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7844b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7844b-126">-WhatIf</span></span>
<span data-ttu-id="7844b-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7844b-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7844b-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7844b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7844b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7844b-129">CommonParameters</span></span>
<span data-ttu-id="7844b-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7844b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7844b-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7844b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7844b-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7844b-132">INPUTS</span></span>

### <span data-ttu-id="7844b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="7844b-133">System.String</span></span>

## <span data-ttu-id="7844b-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7844b-134">OUTPUTS</span></span>

### <span data-ttu-id="7844b-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7844b-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="7844b-136">Note</span><span class="sxs-lookup"><span data-stu-id="7844b-136">NOTES</span></span>

## <span data-ttu-id="7844b-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7844b-137">RELATED LINKS</span></span>

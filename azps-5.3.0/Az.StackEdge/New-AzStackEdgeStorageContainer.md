---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageContainer.md
ms.openlocfilehash: 5c0af3ed67bd7cba3408b6628de70c7064120954
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380978"
---
# <span data-ttu-id="b6a9e-101">New-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b6a9e-101">New-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="b6a9e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b6a9e-102">SYNOPSIS</span></span>
<span data-ttu-id="b6a9e-103">Crea un nuovo contenitore di archiviazione nell'account di archiviazione perimetrale nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b6a9e-103">Creates a new storage container in the Edge Storage account on the device.</span></span>

## <span data-ttu-id="b6a9e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6a9e-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-DataFormat <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6a9e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6a9e-105">DESCRIPTION</span></span>
<span data-ttu-id="b6a9e-106">Il cmdlet **New-AzStackEdgeStorageContainer** crea un nuovo contenitore di archiviazione nell'account di archiviazione perimetrale in un dispositivo di bordo dello stack.</span><span class="sxs-lookup"><span data-stu-id="b6a9e-106">The **New-AzStackEdgeStorageContainer** cmdlet creates a new storage container in the Edge Storage account on a Stack Edge device.</span></span>

## <span data-ttu-id="b6a9e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6a9e-107">EXAMPLES</span></span>

### <span data-ttu-id="b6a9e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b6a9e-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name edgecontainer1 -DataFormat BlockBlob
Name       DataFormat EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ---------------------- ---------- -----------------
container1 BlockBlob  edgestorageaccount1    db-edge    resourceGroupName
```

## <span data-ttu-id="b6a9e-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b6a9e-109">PARAMETERS</span></span>

### <span data-ttu-id="b6a9e-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6a9e-110">-AsJob</span></span>
<span data-ttu-id="b6a9e-111">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b6a9e-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b6a9e-112">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="b6a9e-112">-DataFormat</span></span>
<span data-ttu-id="b6a9e-113">Impostare il formato dati ex: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="b6a9e-113">Set Data Format ex: PageBlob, BlobBlob</span></span>

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

### <span data-ttu-id="b6a9e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6a9e-114">-DefaultProfile</span></span>
<span data-ttu-id="b6a9e-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b6a9e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6a9e-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b6a9e-116">-DeviceName</span></span>
<span data-ttu-id="b6a9e-117">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="b6a9e-117">Device Name</span></span>

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

### <span data-ttu-id="b6a9e-118">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b6a9e-118">-EdgeStorageAccountName</span></span>
<span data-ttu-id="b6a9e-119">Fornisci il nome di EdgeStorageAccount esistente</span><span class="sxs-lookup"><span data-stu-id="b6a9e-119">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="b6a9e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b6a9e-120">-Name</span></span>
<span data-ttu-id="b6a9e-121">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="b6a9e-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6a9e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6a9e-122">-ResourceGroupName</span></span>
<span data-ttu-id="b6a9e-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="b6a9e-123">Resource Group Name</span></span>

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

### <span data-ttu-id="b6a9e-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b6a9e-124">-Confirm</span></span>
<span data-ttu-id="b6a9e-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6a9e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6a9e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6a9e-126">-WhatIf</span></span>
<span data-ttu-id="b6a9e-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6a9e-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b6a9e-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6a9e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6a9e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6a9e-129">CommonParameters</span></span>
<span data-ttu-id="b6a9e-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6a9e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6a9e-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6a9e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6a9e-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b6a9e-132">INPUTS</span></span>

### <span data-ttu-id="b6a9e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b6a9e-133">System.String</span></span>

## <span data-ttu-id="b6a9e-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6a9e-134">OUTPUTS</span></span>

### <span data-ttu-id="b6a9e-135">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b6a9e-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="b6a9e-136">Note</span><span class="sxs-lookup"><span data-stu-id="b6a9e-136">NOTES</span></span>

## <span data-ttu-id="b6a9e-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6a9e-137">RELATED LINKS</span></span>

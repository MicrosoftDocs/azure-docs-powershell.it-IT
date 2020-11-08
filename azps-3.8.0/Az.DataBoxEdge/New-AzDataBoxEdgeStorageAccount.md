---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 2a5a1314f422a7b91a5cc8885abe0af98fa395a2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021349"
---
# <span data-ttu-id="e7bb6-101">New-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e7bb6-101">New-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="e7bb6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e7bb6-102">SYNOPSIS</span></span>
<span data-ttu-id="e7bb6-103">Crea un nuovo account di archiviazione Edge nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e7bb6-103">Creates a new Edge Storage account in the device.</span></span>

## <span data-ttu-id="e7bb6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e7bb6-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountCredentialName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-Cloud] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7bb6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7bb6-105">DESCRIPTION</span></span>
<span data-ttu-id="e7bb6-106">Il cmdlet **New-AzDataBoxEdgeStorageAccount** crea un nuovo account di archiviazione Edge in un dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="e7bb6-106">The **New-AzDataBoxEdgeStorageAccount** cmdlet creates a new Edge Storage account in a Data Box Edge device.</span></span> <span data-ttu-id="e7bb6-107">Per un dispositivo, è possibile eseguire il mapping di un account di archiviazione Edge al massimo a un solo account di archiviazione cloud.</span><span class="sxs-lookup"><span data-stu-id="e7bb6-107">For a device, one Edge Storage account can be mapped at most to only one Cloud Storage account.</span></span>

## <span data-ttu-id="e7bb6-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e7bb6-108">EXAMPLES</span></span>

### <span data-ttu-id="e7bb6-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e7bb6-109">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount1 -StorageAccountCredentialName cloudstorageaccount1 -Cloud
Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 0              OK     https://edgestoragegacount1.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount1     dbEdge     resourceGroupName
```

### <span data-ttu-id="e7bb6-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e7bb6-110">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount2 -StorageAccountCredentialName cloudstorageaccount2

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount2     dbEdge     resourceGroupName
```

<span data-ttu-id="e7bb6-111">2 EdgeStorageAccounts nel dispositivo non è possibile condividere più di un account di archiviazione cloud</span><span class="sxs-lookup"><span data-stu-id="e7bb6-111">2 EdgeStorageAccounts on the device cannot share more than 1 Cloud Storage Account</span></span>

## <span data-ttu-id="e7bb6-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e7bb6-112">PARAMETERS</span></span>

### <span data-ttu-id="e7bb6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e7bb6-113">-AsJob</span></span>
<span data-ttu-id="e7bb6-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e7bb6-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e7bb6-115">-Cloud</span><span class="sxs-lookup"><span data-stu-id="e7bb6-115">-Cloud</span></span>
<span data-ttu-id="e7bb6-116">Userà un CloudStorageAccount per il tiering</span><span class="sxs-lookup"><span data-stu-id="e7bb6-116">Will use a CloudStorageAccount for tiering</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7bb6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7bb6-117">-DefaultProfile</span></span>
<span data-ttu-id="e7bb6-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e7bb6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7bb6-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e7bb6-119">-DeviceName</span></span>
<span data-ttu-id="e7bb6-120">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="e7bb6-120">Device Name</span></span>

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

### <span data-ttu-id="e7bb6-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e7bb6-121">-Name</span></span>
<span data-ttu-id="e7bb6-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="e7bb6-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7bb6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7bb6-123">-ResourceGroupName</span></span>
<span data-ttu-id="e7bb6-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="e7bb6-124">Resource Group Name</span></span>

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

### <span data-ttu-id="e7bb6-125">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="e7bb6-125">-StorageAccountCredentialName</span></span>
<span data-ttu-id="e7bb6-126">Specificare il nome della risorsa di StorageAccountCredential esistente</span><span class="sxs-lookup"><span data-stu-id="e7bb6-126">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7bb6-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e7bb6-127">-Confirm</span></span>
<span data-ttu-id="e7bb6-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7bb6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7bb6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7bb6-129">-WhatIf</span></span>
<span data-ttu-id="e7bb6-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e7bb6-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e7bb6-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e7bb6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7bb6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7bb6-132">CommonParameters</span></span>
<span data-ttu-id="e7bb6-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7bb6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7bb6-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7bb6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7bb6-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e7bb6-135">INPUTS</span></span>

### <span data-ttu-id="e7bb6-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e7bb6-136">System.String</span></span>

### <span data-ttu-id="e7bb6-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e7bb6-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e7bb6-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e7bb6-138">OUTPUTS</span></span>

### <span data-ttu-id="e7bb6-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e7bb6-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="e7bb6-140">Note</span><span class="sxs-lookup"><span data-stu-id="e7bb6-140">NOTES</span></span>

## <span data-ttu-id="e7bb6-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e7bb6-141">RELATED LINKS</span></span>

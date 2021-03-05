---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/new-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccount.md
ms.openlocfilehash: f35e94aab5bdb59a2cc6d4c8e38cee1142c2b47a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005261"
---
# <span data-ttu-id="318cf-101">New-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="318cf-101">New-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="318cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="318cf-102">SYNOPSIS</span></span>
<span data-ttu-id="318cf-103">Crea un nuovo account di Archiviazione Edge nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="318cf-103">Creates a new Edge Storage account in the device.</span></span>

## <span data-ttu-id="318cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="318cf-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountCredentialName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-Cloud] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="318cf-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="318cf-105">DESCRIPTION</span></span>
<span data-ttu-id="318cf-106">Il cmdlet **New-AzStackEdgeStorageAccount** crea un nuovo account di Archiviazione Edge in un dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="318cf-106">The **New-AzStackEdgeStorageAccount** cmdlet creates a new Edge Storage account in a Stack Edge device.</span></span> <span data-ttu-id="318cf-107">Per un dispositivo, è possibile eseguire il mapping di un account di Archiviazione Edge al massimo a un solo account di Archiviazione cloud.</span><span class="sxs-lookup"><span data-stu-id="318cf-107">For a device, one Edge Storage account can be mapped at most to only one Cloud Storage account.</span></span>

## <span data-ttu-id="318cf-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="318cf-108">EXAMPLES</span></span>

### <span data-ttu-id="318cf-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="318cf-109">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount1 -StorageAccountCredentialName cloudstorageaccount1 -Cloud
Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 0              OK     https://edgestoragegacount1.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount1     dbEdge     resourceGroupName
```

### <span data-ttu-id="318cf-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="318cf-110">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount2 -StorageAccountCredentialName cloudstorageaccount2

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount2     dbEdge     resourceGroupName
```

<span data-ttu-id="318cf-111">2 EdgeStorageAccounts nel dispositivo non possono condividere più di 1 account di archiviazione cloud</span><span class="sxs-lookup"><span data-stu-id="318cf-111">2 EdgeStorageAccounts on the device cannot share more than 1 Cloud Storage Account</span></span>

## <span data-ttu-id="318cf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="318cf-112">PARAMETERS</span></span>

### <span data-ttu-id="318cf-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="318cf-113">-AsJob</span></span>
<span data-ttu-id="318cf-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="318cf-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="318cf-115">-Cloud</span><span class="sxs-lookup"><span data-stu-id="318cf-115">-Cloud</span></span>
<span data-ttu-id="318cf-116">Userà un CloudStorageAccount per il tiering</span><span class="sxs-lookup"><span data-stu-id="318cf-116">Will use a CloudStorageAccount for tiering</span></span>

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

### <span data-ttu-id="318cf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="318cf-117">-DefaultProfile</span></span>
<span data-ttu-id="318cf-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="318cf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="318cf-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="318cf-119">-DeviceName</span></span>
<span data-ttu-id="318cf-120">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="318cf-120">Device Name</span></span>

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

### <span data-ttu-id="318cf-121">-Name</span><span class="sxs-lookup"><span data-stu-id="318cf-121">-Name</span></span>
<span data-ttu-id="318cf-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="318cf-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EdgeStorageAccount

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="318cf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="318cf-123">-ResourceGroupName</span></span>
<span data-ttu-id="318cf-124">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="318cf-124">Resource Group Name</span></span>

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

### <span data-ttu-id="318cf-125">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="318cf-125">-StorageAccountCredentialName</span></span>
<span data-ttu-id="318cf-126">Fornire il nome della risorsa StorageAccountCredential esistente</span><span class="sxs-lookup"><span data-stu-id="318cf-126">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="318cf-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="318cf-127">-Confirm</span></span>
<span data-ttu-id="318cf-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="318cf-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="318cf-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="318cf-129">-WhatIf</span></span>
<span data-ttu-id="318cf-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="318cf-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="318cf-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="318cf-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="318cf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="318cf-132">CommonParameters</span></span>
<span data-ttu-id="318cf-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="318cf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="318cf-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="318cf-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="318cf-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="318cf-135">INPUTS</span></span>

### <span data-ttu-id="318cf-136">System.String</span><span class="sxs-lookup"><span data-stu-id="318cf-136">System.String</span></span>

### <span data-ttu-id="318cf-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="318cf-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="318cf-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="318cf-138">OUTPUTS</span></span>

### <span data-ttu-id="318cf-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="318cf-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="318cf-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="318cf-140">NOTES</span></span>

## <span data-ttu-id="318cf-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="318cf-141">RELATED LINKS</span></span>

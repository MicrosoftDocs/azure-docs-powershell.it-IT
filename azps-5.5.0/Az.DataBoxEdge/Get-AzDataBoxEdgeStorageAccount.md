---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 7b797b4088cab20ee1933ce88a2462288f04653e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194910"
---
# <span data-ttu-id="c23a1-101">Get-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c23a1-101">Get-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="c23a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c23a1-102">SYNOPSIS</span></span>
<span data-ttu-id="c23a1-103">Recupera gli account di Archiviazione Edge nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c23a1-103">Gets the Edge Storage accounts on the device.</span></span>

## <span data-ttu-id="c23a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c23a1-104">SYNTAX</span></span>

### <span data-ttu-id="c23a1-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c23a1-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c23a1-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c23a1-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c23a1-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c23a1-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c23a1-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c23a1-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="c23a1-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c23a1-109">DESCRIPTION</span></span>
<span data-ttu-id="c23a1-110">Il cmdlet **Get-AzDataBoxEdgeStorageAccount** ottiene gli account di Archiviazione Edge disponibili in un dispositivo Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="c23a1-110">The **Get-AzDataBoxEdgeStorageAccount** cmdlet gets the Edge Storage accounts available on a Data Box Edge device.</span></span> <span data-ttu-id="c23a1-111">È possibile specificare il nome come parametro nel cmdlet per ottenere le informazioni di uno specifico account di Archiviazione Edge.</span><span class="sxs-lookup"><span data-stu-id="c23a1-111">You can specify the Name as a parameter in the cmdlet to get the information of a specific Edge Storage account.</span></span>

## <span data-ttu-id="c23a1-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c23a1-112">EXAMPLES</span></span>

### <span data-ttu-id="c23a1-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c23a1-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge -Name edgestoragegacount1

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName
```

### <span data-ttu-id="c23a1-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c23a1-114">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="c23a1-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="c23a1-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeDevice -ResourceGroupName rgpName -DeviceName db-edge | Get-AzDataBoxEdgeStorageAccount

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="c23a1-116">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="c23a1-116">Example 4</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -DeviceObject $dbEdge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

## <span data-ttu-id="c23a1-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c23a1-117">PARAMETERS</span></span>

### <span data-ttu-id="c23a1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c23a1-118">-DefaultProfile</span></span>
<span data-ttu-id="c23a1-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c23a1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c23a1-120">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="c23a1-120">-DeviceName</span></span>
<span data-ttu-id="c23a1-121">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="c23a1-121">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c23a1-122">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="c23a1-122">-DeviceObject</span></span>
<span data-ttu-id="c23a1-123">Specifica l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="c23a1-123">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c23a1-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c23a1-124">-Name</span></span>
<span data-ttu-id="c23a1-125">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="c23a1-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeStorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeStorageAccountName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c23a1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c23a1-126">-ResourceGroupName</span></span>
<span data-ttu-id="c23a1-127">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="c23a1-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c23a1-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c23a1-128">-ResourceId</span></span>
<span data-ttu-id="c23a1-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="c23a1-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c23a1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c23a1-130">CommonParameters</span></span>
<span data-ttu-id="c23a1-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c23a1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c23a1-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c23a1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c23a1-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="c23a1-133">INPUTS</span></span>

### <span data-ttu-id="c23a1-134">System.String</span><span class="sxs-lookup"><span data-stu-id="c23a1-134">System.String</span></span>

### <span data-ttu-id="c23a1-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="c23a1-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="c23a1-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c23a1-136">OUTPUTS</span></span>

### <span data-ttu-id="c23a1-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c23a1-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="c23a1-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="c23a1-138">NOTES</span></span>

## <span data-ttu-id="c23a1-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c23a1-139">RELATED LINKS</span></span>

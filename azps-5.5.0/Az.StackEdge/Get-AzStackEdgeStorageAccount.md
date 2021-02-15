---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
ms.openlocfilehash: 59d01af85279414503b765aea7f326a8670ec1c2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195847"
---
# <span data-ttu-id="01186-101">Get-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="01186-101">Get-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="01186-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01186-102">SYNOPSIS</span></span>
<span data-ttu-id="01186-103">Recupera gli account di Archiviazione Edge nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="01186-103">Gets the Edge Storage accounts on the device.</span></span>

## <span data-ttu-id="01186-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="01186-104">SYNTAX</span></span>

### <span data-ttu-id="01186-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="01186-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01186-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="01186-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="01186-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="01186-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01186-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01186-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="01186-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="01186-109">DESCRIPTION</span></span>
<span data-ttu-id="01186-110">Il cmdlet **Get-AzStackEdgeStorageAccount** ottiene gli account di Archiviazione Edge disponibili in un dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="01186-110">The **Get-AzStackEdgeStorageAccount** cmdlet gets the Edge Storage accounts available on a Stack Edge device.</span></span> <span data-ttu-id="01186-111">È possibile specificare il nome come parametro nel cmdlet per ottenere le informazioni di uno specifico account di Archiviazione Edge.</span><span class="sxs-lookup"><span data-stu-id="01186-111">You can specify the Name as a parameter in the cmdlet to get the information of a specific Edge Storage account.</span></span>

## <span data-ttu-id="01186-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="01186-112">EXAMPLES</span></span>

### <span data-ttu-id="01186-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="01186-113">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge -Name edgestoragegacount1

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName
```

### <span data-ttu-id="01186-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="01186-114">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="01186-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="01186-115">Example 3</span></span>
```powershell
PS C:\> Get-AzStackEdgeDevice -ResourceGroupName rgpName -DeviceName db-edge | Get-AzStackEdgeStorageAccount

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="01186-116">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="01186-116">Example 4</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -DeviceObject $dbEdge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

## <span data-ttu-id="01186-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01186-117">PARAMETERS</span></span>

### <span data-ttu-id="01186-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01186-118">-DefaultProfile</span></span>
<span data-ttu-id="01186-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="01186-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01186-120">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="01186-120">-DeviceName</span></span>
<span data-ttu-id="01186-121">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="01186-121">Device Name</span></span>

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

### <span data-ttu-id="01186-122">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="01186-122">-DeviceObject</span></span>
<span data-ttu-id="01186-123">Specifica l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="01186-123">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01186-124">-Name</span><span class="sxs-lookup"><span data-stu-id="01186-124">-Name</span></span>
<span data-ttu-id="01186-125">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="01186-125">Resource Name</span></span>

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

### <span data-ttu-id="01186-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01186-126">-ResourceGroupName</span></span>
<span data-ttu-id="01186-127">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="01186-127">Resource Group Name</span></span>

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

### <span data-ttu-id="01186-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01186-128">-ResourceId</span></span>
<span data-ttu-id="01186-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="01186-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="01186-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01186-130">CommonParameters</span></span>
<span data-ttu-id="01186-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01186-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01186-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="01186-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01186-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="01186-133">INPUTS</span></span>

### <span data-ttu-id="01186-134">System.String</span><span class="sxs-lookup"><span data-stu-id="01186-134">System.String</span></span>

### <span data-ttu-id="01186-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="01186-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="01186-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="01186-136">OUTPUTS</span></span>

### <span data-ttu-id="01186-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="01186-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="01186-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="01186-138">NOTES</span></span>

## <span data-ttu-id="01186-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="01186-139">RELATED LINKS</span></span>

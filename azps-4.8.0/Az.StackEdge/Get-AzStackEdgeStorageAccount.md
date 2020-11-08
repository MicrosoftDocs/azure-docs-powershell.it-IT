---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
ms.openlocfilehash: 59d01af85279414503b765aea7f326a8670ec1c2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188754"
---
# <span data-ttu-id="a6c68-101">Get-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6c68-101">Get-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="a6c68-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a6c68-102">SYNOPSIS</span></span>
<span data-ttu-id="a6c68-103">Ottiene gli account di archiviazione Edge nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a6c68-103">Gets the Edge Storage accounts on the device.</span></span>

## <span data-ttu-id="a6c68-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6c68-104">SYNTAX</span></span>

### <span data-ttu-id="a6c68-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a6c68-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6c68-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6c68-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a6c68-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6c68-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6c68-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6c68-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="a6c68-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6c68-109">DESCRIPTION</span></span>
<span data-ttu-id="a6c68-110">Il cmdlet **Get-AzStackEdgeStorageAccount** ottiene gli account di archiviazione Edge disponibili in un dispositivo di bordo dello stack.</span><span class="sxs-lookup"><span data-stu-id="a6c68-110">The **Get-AzStackEdgeStorageAccount** cmdlet gets the Edge Storage accounts available on a Stack Edge device.</span></span> <span data-ttu-id="a6c68-111">Puoi specificare il nome come parametro nel cmdlet per ottenere le informazioni di un account di archiviazione Edge specifico.</span><span class="sxs-lookup"><span data-stu-id="a6c68-111">You can specify the Name as a parameter in the cmdlet to get the information of a specific Edge Storage account.</span></span>

## <span data-ttu-id="a6c68-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6c68-112">EXAMPLES</span></span>

### <span data-ttu-id="a6c68-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a6c68-113">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge -Name edgestoragegacount1

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName
```

### <span data-ttu-id="a6c68-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a6c68-114">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="a6c68-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="a6c68-115">Example 3</span></span>
```powershell
PS C:\> Get-AzStackEdgeDevice -ResourceGroupName rgpName -DeviceName db-edge | Get-AzStackEdgeStorageAccount

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="a6c68-116">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="a6c68-116">Example 4</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -DeviceObject $dbEdge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

## <span data-ttu-id="a6c68-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a6c68-117">PARAMETERS</span></span>

### <span data-ttu-id="a6c68-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6c68-118">-DefaultProfile</span></span>
<span data-ttu-id="a6c68-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a6c68-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6c68-120">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a6c68-120">-DeviceName</span></span>
<span data-ttu-id="a6c68-121">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="a6c68-121">Device Name</span></span>

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

### <span data-ttu-id="a6c68-122">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="a6c68-122">-DeviceObject</span></span>
<span data-ttu-id="a6c68-123">Immettere l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="a6c68-123">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="a6c68-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="a6c68-124">-Name</span></span>
<span data-ttu-id="a6c68-125">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="a6c68-125">Resource Name</span></span>

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

### <span data-ttu-id="a6c68-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6c68-126">-ResourceGroupName</span></span>
<span data-ttu-id="a6c68-127">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="a6c68-127">Resource Group Name</span></span>

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

### <span data-ttu-id="a6c68-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6c68-128">-ResourceId</span></span>
<span data-ttu-id="a6c68-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6c68-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="a6c68-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6c68-130">CommonParameters</span></span>
<span data-ttu-id="a6c68-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6c68-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6c68-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6c68-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6c68-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a6c68-133">INPUTS</span></span>

### <span data-ttu-id="a6c68-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a6c68-134">System.String</span></span>

### <span data-ttu-id="a6c68-135">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="a6c68-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="a6c68-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6c68-136">OUTPUTS</span></span>

### <span data-ttu-id="a6c68-137">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6c68-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="a6c68-138">Note</span><span class="sxs-lookup"><span data-stu-id="a6c68-138">NOTES</span></span>

## <span data-ttu-id="a6c68-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6c68-139">RELATED LINKS</span></span>

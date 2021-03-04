---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/get-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 8dba984529d52dad6d256a5ad40b7594e561f324
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998590"
---
# <span data-ttu-id="88452-101">Get-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="88452-101">Get-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="88452-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88452-102">SYNOPSIS</span></span>
<span data-ttu-id="88452-103">Recupera le credenziali dell'account di archiviazione corrispondenti all'account di archiviazione nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="88452-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="88452-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="88452-104">SYNTAX</span></span>

### <span data-ttu-id="88452-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="88452-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88452-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="88452-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="88452-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="88452-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88452-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88452-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="88452-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="88452-109">DESCRIPTION</span></span>
<span data-ttu-id="88452-110">Il cmdlet **Get-AzDataBoxEdgeStorageAccountCredential** ottiene le credenziali dell'account di archiviazione corrispondente nel dispositivo Edge di Data Box.</span><span class="sxs-lookup"><span data-stu-id="88452-110">The **Get-AzDataBoxEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Data Box Edge device.</span></span> <span data-ttu-id="88452-111">È possibile specificare i parametri Nome, Nome gruppo di risorse e Nome dispositivo per ottenere informazioni sulle credenziali di un account di archiviazione specifico.</span><span class="sxs-lookup"><span data-stu-id="88452-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="88452-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="88452-112">EXAMPLES</span></span>

### <span data-ttu-id="88452-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="88452-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="88452-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88452-114">PARAMETERS</span></span>

### <span data-ttu-id="88452-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88452-115">-DefaultProfile</span></span>
<span data-ttu-id="88452-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="88452-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88452-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="88452-117">-DeviceName</span></span>
<span data-ttu-id="88452-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="88452-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88452-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="88452-119">-DeviceObject</span></span>
<span data-ttu-id="88452-120">Specifica l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="88452-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="88452-121">-Name</span><span class="sxs-lookup"><span data-stu-id="88452-121">-Name</span></span>
<span data-ttu-id="88452-122">Nome dell'account di archiviazione da usare</span><span class="sxs-lookup"><span data-stu-id="88452-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88452-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88452-123">-ResourceGroupName</span></span>
<span data-ttu-id="88452-124">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="88452-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88452-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88452-125">-ResourceId</span></span>
<span data-ttu-id="88452-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="88452-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88452-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88452-127">CommonParameters</span></span>
<span data-ttu-id="88452-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88452-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88452-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="88452-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88452-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="88452-130">INPUTS</span></span>

### <span data-ttu-id="88452-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="88452-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="88452-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="88452-132">OUTPUTS</span></span>

### <span data-ttu-id="88452-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="88452-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="88452-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="88452-134">NOTES</span></span>

## <span data-ttu-id="88452-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="88452-135">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: eca1227150741814178dbabe25caff79b3c3381e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208795"
---
# <span data-ttu-id="1af45-101">Get-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="1af45-101">Get-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="1af45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1af45-102">SYNOPSIS</span></span>
<span data-ttu-id="1af45-103">Recupera le credenziali dell'account di archiviazione corrispondenti all'account di archiviazione nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1af45-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="1af45-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1af45-104">SYNTAX</span></span>

### <span data-ttu-id="1af45-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1af45-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1af45-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1af45-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1af45-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1af45-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1af45-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1af45-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="1af45-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1af45-109">DESCRIPTION</span></span>
<span data-ttu-id="1af45-110">Il cmdlet **Get-AzDataBoxEdgeStorageAccountCredential** ottiene le credenziali dell'account di archiviazione corrispondente nel dispositivo Edge di Data Box.</span><span class="sxs-lookup"><span data-stu-id="1af45-110">The **Get-AzDataBoxEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Data Box Edge device.</span></span> <span data-ttu-id="1af45-111">È possibile specificare i parametri Nome, Nome gruppo di risorse e Nome dispositivo per ottenere informazioni sulle credenziali di un account di archiviazione specifico.</span><span class="sxs-lookup"><span data-stu-id="1af45-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="1af45-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1af45-112">EXAMPLES</span></span>

### <span data-ttu-id="1af45-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1af45-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="1af45-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1af45-114">PARAMETERS</span></span>

### <span data-ttu-id="1af45-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1af45-115">-DefaultProfile</span></span>
<span data-ttu-id="1af45-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1af45-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1af45-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="1af45-117">-DeviceName</span></span>
<span data-ttu-id="1af45-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="1af45-118">Device Name</span></span>

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

### <span data-ttu-id="1af45-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="1af45-119">-DeviceObject</span></span>
<span data-ttu-id="1af45-120">Specifica l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="1af45-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="1af45-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1af45-121">-Name</span></span>
<span data-ttu-id="1af45-122">Nome dell'account di archiviazione da usare</span><span class="sxs-lookup"><span data-stu-id="1af45-122">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="1af45-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1af45-123">-ResourceGroupName</span></span>
<span data-ttu-id="1af45-124">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="1af45-124">Resource Group Name</span></span>

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

### <span data-ttu-id="1af45-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1af45-125">-ResourceId</span></span>
<span data-ttu-id="1af45-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="1af45-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="1af45-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1af45-127">CommonParameters</span></span>
<span data-ttu-id="1af45-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1af45-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1af45-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1af45-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1af45-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="1af45-130">INPUTS</span></span>

### <span data-ttu-id="1af45-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="1af45-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="1af45-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1af45-132">OUTPUTS</span></span>

### <span data-ttu-id="1af45-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="1af45-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="1af45-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="1af45-134">NOTES</span></span>

## <span data-ttu-id="1af45-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1af45-135">RELATED LINKS</span></span>

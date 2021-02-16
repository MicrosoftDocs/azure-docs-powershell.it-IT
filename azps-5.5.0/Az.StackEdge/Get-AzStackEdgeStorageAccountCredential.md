---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: f198db6a49e1f5165dcfcd4effd91106cc0df831
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176686"
---
# <span data-ttu-id="c1af0-101">Get-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="c1af0-101">Get-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="c1af0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1af0-102">SYNOPSIS</span></span>
<span data-ttu-id="c1af0-103">Recupera le credenziali dell'account di archiviazione corrispondenti all'account di archiviazione nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c1af0-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="c1af0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c1af0-104">SYNTAX</span></span>

### <span data-ttu-id="c1af0-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c1af0-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1af0-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1af0-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c1af0-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1af0-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1af0-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1af0-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="c1af0-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c1af0-109">DESCRIPTION</span></span>
<span data-ttu-id="c1af0-110">Il cmdlet **Get-AzStackEdgeStorageAccountCredential** ottiene le credenziali dell'account di archiviazione corrispondente nel dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="c1af0-110">The **Get-AzStackEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Stack Edge device.</span></span> <span data-ttu-id="c1af0-111">È possibile specificare i parametri Nome, Nome gruppo di risorse e Nome dispositivo per ottenere informazioni sulle credenziali di un account di archiviazione specifico.</span><span class="sxs-lookup"><span data-stu-id="c1af0-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="c1af0-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c1af0-112">EXAMPLES</span></span>

### <span data-ttu-id="c1af0-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c1af0-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="c1af0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1af0-114">PARAMETERS</span></span>

### <span data-ttu-id="c1af0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1af0-115">-DefaultProfile</span></span>
<span data-ttu-id="c1af0-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c1af0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1af0-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="c1af0-117">-DeviceName</span></span>
<span data-ttu-id="c1af0-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="c1af0-118">Device Name</span></span>

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

### <span data-ttu-id="c1af0-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="c1af0-119">-DeviceObject</span></span>
<span data-ttu-id="c1af0-120">Specifica l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="c1af0-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="c1af0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c1af0-121">-Name</span></span>
<span data-ttu-id="c1af0-122">Nome dell'account di archiviazione da usare</span><span class="sxs-lookup"><span data-stu-id="c1af0-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: StorageAccountCredentialName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1af0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1af0-123">-ResourceGroupName</span></span>
<span data-ttu-id="c1af0-124">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="c1af0-124">Resource Group Name</span></span>

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

### <span data-ttu-id="c1af0-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1af0-125">-ResourceId</span></span>
<span data-ttu-id="c1af0-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1af0-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="c1af0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1af0-127">CommonParameters</span></span>
<span data-ttu-id="c1af0-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1af0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1af0-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c1af0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1af0-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="c1af0-130">INPUTS</span></span>

### <span data-ttu-id="c1af0-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="c1af0-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="c1af0-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c1af0-132">OUTPUTS</span></span>

### <span data-ttu-id="c1af0-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="c1af0-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="c1af0-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="c1af0-134">NOTES</span></span>

## <span data-ttu-id="c1af0-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c1af0-135">RELATED LINKS</span></span>

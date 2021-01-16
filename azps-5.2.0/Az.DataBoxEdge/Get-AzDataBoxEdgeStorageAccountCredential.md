---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: eca1227150741814178dbabe25caff79b3c3381e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366040"
---
# <span data-ttu-id="f475e-101">Get-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="f475e-101">Get-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="f475e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f475e-102">SYNOPSIS</span></span>
<span data-ttu-id="f475e-103">Ottiene le credenziali dell'account di archiviazione corrispondenti all'account di archiviazione nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f475e-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="f475e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f475e-104">SYNTAX</span></span>

### <span data-ttu-id="f475e-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f475e-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f475e-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f475e-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f475e-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f475e-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f475e-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f475e-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="f475e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f475e-109">DESCRIPTION</span></span>
<span data-ttu-id="f475e-110">Il cmdlet **Get-AzDataBoxEdgeStorageAccountCredential** ottiene le credenziali dell'account di archiviazione per l'account di archiviazione corrispondente nel dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="f475e-110">The **Get-AzDataBoxEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Data Box Edge device.</span></span> <span data-ttu-id="f475e-111">Puoi specificare i parametri nome, nome del gruppo di risorse e nome dispositivo per ottenere informazioni su una specifica credenziale dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f475e-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="f475e-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f475e-112">EXAMPLES</span></span>

### <span data-ttu-id="f475e-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f475e-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="f475e-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f475e-114">PARAMETERS</span></span>

### <span data-ttu-id="f475e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f475e-115">-DefaultProfile</span></span>
<span data-ttu-id="f475e-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f475e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f475e-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f475e-117">-DeviceName</span></span>
<span data-ttu-id="f475e-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="f475e-118">Device Name</span></span>

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

### <span data-ttu-id="f475e-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="f475e-119">-DeviceObject</span></span>
<span data-ttu-id="f475e-120">Immettere l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="f475e-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="f475e-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="f475e-121">-Name</span></span>
<span data-ttu-id="f475e-122">Nome dell'account di archiviazione da usare</span><span class="sxs-lookup"><span data-stu-id="f475e-122">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="f475e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f475e-123">-ResourceGroupName</span></span>
<span data-ttu-id="f475e-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="f475e-124">Resource Group Name</span></span>

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

### <span data-ttu-id="f475e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f475e-125">-ResourceId</span></span>
<span data-ttu-id="f475e-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="f475e-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="f475e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f475e-127">CommonParameters</span></span>
<span data-ttu-id="f475e-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f475e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f475e-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f475e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f475e-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f475e-130">INPUTS</span></span>

### <span data-ttu-id="f475e-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="f475e-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="f475e-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f475e-132">OUTPUTS</span></span>

### <span data-ttu-id="f475e-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="f475e-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="f475e-134">Note</span><span class="sxs-lookup"><span data-stu-id="f475e-134">NOTES</span></span>

## <span data-ttu-id="f475e-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f475e-135">RELATED LINKS</span></span>

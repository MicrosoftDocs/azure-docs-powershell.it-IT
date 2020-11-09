---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: f198db6a49e1f5165dcfcd4effd91106cc0df831
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301741"
---
# <span data-ttu-id="c6891-101">Get-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="c6891-101">Get-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="c6891-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c6891-102">SYNOPSIS</span></span>
<span data-ttu-id="c6891-103">Ottiene le credenziali dell'account di archiviazione corrispondenti all'account di archiviazione nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c6891-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="c6891-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c6891-104">SYNTAX</span></span>

### <span data-ttu-id="c6891-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c6891-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6891-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6891-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c6891-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6891-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6891-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6891-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="c6891-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c6891-109">DESCRIPTION</span></span>
<span data-ttu-id="c6891-110">Il cmdlet **Get-AzStackEdgeStorageAccountCredential** ottiene le credenziali dell'account di archiviazione per l'account di archiviazione corrispondente nel dispositivo dello stack Edge.</span><span class="sxs-lookup"><span data-stu-id="c6891-110">The **Get-AzStackEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Stack Edge device.</span></span> <span data-ttu-id="c6891-111">Puoi specificare i parametri nome, nome del gruppo di risorse e nome dispositivo per ottenere informazioni su una specifica credenziale dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c6891-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="c6891-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c6891-112">EXAMPLES</span></span>

### <span data-ttu-id="c6891-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c6891-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="c6891-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c6891-114">PARAMETERS</span></span>

### <span data-ttu-id="c6891-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6891-115">-DefaultProfile</span></span>
<span data-ttu-id="c6891-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c6891-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6891-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="c6891-117">-DeviceName</span></span>
<span data-ttu-id="c6891-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="c6891-118">Device Name</span></span>

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

### <span data-ttu-id="c6891-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="c6891-119">-DeviceObject</span></span>
<span data-ttu-id="c6891-120">Immettere l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="c6891-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="c6891-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="c6891-121">-Name</span></span>
<span data-ttu-id="c6891-122">Nome dell'account di archiviazione da usare</span><span class="sxs-lookup"><span data-stu-id="c6891-122">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="c6891-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6891-123">-ResourceGroupName</span></span>
<span data-ttu-id="c6891-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="c6891-124">Resource Group Name</span></span>

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

### <span data-ttu-id="c6891-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6891-125">-ResourceId</span></span>
<span data-ttu-id="c6891-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6891-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="c6891-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6891-127">CommonParameters</span></span>
<span data-ttu-id="c6891-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6891-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6891-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6891-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6891-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c6891-130">INPUTS</span></span>

### <span data-ttu-id="c6891-131">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="c6891-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="c6891-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c6891-132">OUTPUTS</span></span>

### <span data-ttu-id="c6891-133">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="c6891-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="c6891-134">Note</span><span class="sxs-lookup"><span data-stu-id="c6891-134">NOTES</span></span>

## <span data-ttu-id="c6891-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c6891-135">RELATED LINKS</span></span>

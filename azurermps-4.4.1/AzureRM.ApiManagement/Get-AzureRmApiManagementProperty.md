---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
ms.openlocfilehash: 7542e9621d90ffdb19bb8db679592dd17a216d5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686241"
---
# <span data-ttu-id="77b0d-101">Get-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="77b0d-101">Get-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="77b0d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="77b0d-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77b0d-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="77b0d-103">SYNTAX</span></span>

### <span data-ttu-id="77b0d-104">Ottieni tutte le proprietà (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="77b0d-104">Get all properties (Default)</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="77b0d-105">Ottieni per ID proprietà</span><span class="sxs-lookup"><span data-stu-id="77b0d-105">Get by property ID</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77b0d-106">Trovare le proprietà che contengono il nome</span><span class="sxs-lookup"><span data-stu-id="77b0d-106">Find properties containing Name</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77b0d-107">Trovare le proprietà per tag</span><span class="sxs-lookup"><span data-stu-id="77b0d-107">Find properties by Tag</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77b0d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77b0d-108">DESCRIPTION</span></span>

## <span data-ttu-id="77b0d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="77b0d-109">EXAMPLES</span></span>

### <span data-ttu-id="77b0d-110">1:</span><span class="sxs-lookup"><span data-stu-id="77b0d-110">1:</span></span>
```
PS C:\> Get-AzureRmApiManagementProperty -Context $Context -Name $PropertyName
```

## <span data-ttu-id="77b0d-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="77b0d-111">PARAMETERS</span></span>

### <span data-ttu-id="77b0d-112">-Contesto</span><span class="sxs-lookup"><span data-stu-id="77b0d-112">-Context</span></span>
```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77b0d-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="77b0d-113">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: Find properties containing Name
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77b0d-114">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="77b0d-114">-PropertyId</span></span>
```yaml
Type: System.String
Parameter Sets: Get by property ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77b0d-115">-Tag</span><span class="sxs-lookup"><span data-stu-id="77b0d-115">-Tag</span></span>
<span data-ttu-id="77b0d-116">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="77b0d-116">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="77b0d-117">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="77b0d-117">For example:</span></span>

<span data-ttu-id="77b0d-118">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="77b0d-118">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.String
Parameter Sets: Find properties by Tag
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77b0d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77b0d-119">-DefaultProfile</span></span>
<span data-ttu-id="77b0d-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="77b0d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b0d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77b0d-121">CommonParameters</span></span>
<span data-ttu-id="77b0d-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77b0d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77b0d-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77b0d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77b0d-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="77b0d-124">INPUTS</span></span>

## <span data-ttu-id="77b0d-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="77b0d-125">OUTPUTS</span></span>

### <span data-ttu-id="77b0d-126">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty]</span><span class="sxs-lookup"><span data-stu-id="77b0d-126">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty]</span></span>

### <span data-ttu-id="77b0d-127">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="77b0d-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="77b0d-128">Note</span><span class="sxs-lookup"><span data-stu-id="77b0d-128">NOTES</span></span>

## <span data-ttu-id="77b0d-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="77b0d-129">RELATED LINKS</span></span>


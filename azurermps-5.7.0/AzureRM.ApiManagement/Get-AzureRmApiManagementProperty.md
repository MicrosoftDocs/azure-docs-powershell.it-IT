---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
ms.openlocfilehash: 47167e0729ab3476c74124e16d6ae95901f57ad2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514599"
---
# <span data-ttu-id="7f8fb-101">Get-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="7f8fb-101">Get-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="7f8fb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f8fb-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f8fb-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f8fb-103">SYNTAX</span></span>

### <span data-ttu-id="7f8fb-104">GetAllProperties (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7f8fb-104">GetAllProperties (Default)</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7f8fb-105">GetByPropertyId</span><span class="sxs-lookup"><span data-stu-id="7f8fb-105">GetByPropertyId</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f8fb-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="7f8fb-106">GetByName</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f8fb-107">GetByTag</span><span class="sxs-lookup"><span data-stu-id="7f8fb-107">GetByTag</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f8fb-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f8fb-108">DESCRIPTION</span></span>

## <span data-ttu-id="7f8fb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f8fb-109">EXAMPLES</span></span>

### <span data-ttu-id="7f8fb-110">Esempio 1: ottenere la proprietà per nome</span><span class="sxs-lookup"><span data-stu-id="7f8fb-110">Example 1: Get Property by name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProperty -Context $apimContext -Name "sql-connectionstring"
```

## <span data-ttu-id="7f8fb-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f8fb-111">PARAMETERS</span></span>

### <span data-ttu-id="7f8fb-112">-Contesto</span><span class="sxs-lookup"><span data-stu-id="7f8fb-112">-Context</span></span>
```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f8fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f8fb-113">-DefaultProfile</span></span>
<span data-ttu-id="7f8fb-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7f8fb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f8fb-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f8fb-115">-Name</span></span>
```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f8fb-116">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="7f8fb-116">-PropertyId</span></span>
```yaml
Type: String
Parameter Sets: GetByPropertyId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f8fb-117">-Tag</span><span class="sxs-lookup"><span data-stu-id="7f8fb-117">-Tag</span></span>
<span data-ttu-id="7f8fb-118">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="7f8fb-118">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7f8fb-119">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="7f8fb-119">For example:</span></span>

<span data-ttu-id="7f8fb-120">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="7f8fb-120">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: String
Parameter Sets: GetByTag
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f8fb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f8fb-121">CommonParameters</span></span>
<span data-ttu-id="7f8fb-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f8fb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f8fb-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f8fb-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f8fb-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f8fb-124">INPUTS</span></span>

### <span data-ttu-id="7f8fb-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7f8fb-125">None</span></span>
<span data-ttu-id="7f8fb-126">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="7f8fb-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7f8fb-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f8fb-127">OUTPUTS</span></span>

### <span data-ttu-id="7f8fb-128">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty]</span><span class="sxs-lookup"><span data-stu-id="7f8fb-128">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty]</span></span>

### <span data-ttu-id="7f8fb-129">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="7f8fb-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="7f8fb-130">Note</span><span class="sxs-lookup"><span data-stu-id="7f8fb-130">NOTES</span></span>

## <span data-ttu-id="7f8fb-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f8fb-131">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProperty.md
ms.openlocfilehash: a1ca7766efc79d3d9db2d8feef94a2bb7aab9c36
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019880"
---
# <span data-ttu-id="8c224-101">Get-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="8c224-101">Get-AzApiManagementProperty</span></span>

## <span data-ttu-id="8c224-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8c224-102">SYNOPSIS</span></span>
<span data-ttu-id="8c224-103">Ottiene un elenco o una proprietà specifica (nome-valore).</span><span class="sxs-lookup"><span data-stu-id="8c224-103">Gets a list or a particular Property (Named-Value).</span></span>

## <span data-ttu-id="8c224-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8c224-104">SYNTAX</span></span>

### <span data-ttu-id="8c224-105">GetAllProperties (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8c224-105">GetAllProperties (Default)</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8c224-106">GetByPropertyId</span><span class="sxs-lookup"><span data-stu-id="8c224-106">GetByPropertyId</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c224-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="8c224-107">GetByName</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c224-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="8c224-108">GetByTag</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c224-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8c224-109">DESCRIPTION</span></span>
<span data-ttu-id="8c224-110">Il cmdlet **Get-AzApiManagementProperty** ottiene un elenco o una specifica proprietà.</span><span class="sxs-lookup"><span data-stu-id="8c224-110">The **Get-AzApiManagementProperty** cmdlet gets a list or a particular property.</span></span>

## <span data-ttu-id="8c224-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8c224-111">EXAMPLES</span></span>

### <span data-ttu-id="8c224-112">Esempio 1: ottenere la proprietà per nome</span><span class="sxs-lookup"><span data-stu-id="8c224-112">Example 1: Get Property by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProperty -Context $apimContext -Name "sql-connectionstring"
```

<span data-ttu-id="8c224-113">Questo comando ottiene i dettagli della proprietà in base al nome della proprietà.</span><span class="sxs-lookup"><span data-stu-id="8c224-113">This command gets the property details given the property name.</span></span>

## <span data-ttu-id="8c224-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8c224-114">PARAMETERS</span></span>

### <span data-ttu-id="8c224-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="8c224-115">-Context</span></span>
```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c224-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c224-116">-DefaultProfile</span></span>
<span data-ttu-id="8c224-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8c224-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c224-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="8c224-118">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c224-119">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="8c224-119">-PropertyId</span></span>
```yaml
Type: System.String
Parameter Sets: GetByPropertyId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c224-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="8c224-120">-Tag</span></span>
<span data-ttu-id="8c224-121">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="8c224-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8c224-122">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="8c224-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.String
Parameter Sets: GetByTag
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c224-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c224-123">CommonParameters</span></span>
<span data-ttu-id="8c224-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c224-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c224-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c224-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c224-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8c224-126">INPUTS</span></span>

### <span data-ttu-id="8c224-127">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8c224-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8c224-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8c224-128">System.String</span></span>

## <span data-ttu-id="8c224-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8c224-129">OUTPUTS</span></span>

### <span data-ttu-id="8c224-130">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="8c224-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="8c224-131">Note</span><span class="sxs-lookup"><span data-stu-id="8c224-131">NOTES</span></span>

## <span data-ttu-id="8c224-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8c224-132">RELATED LINKS</span></span>

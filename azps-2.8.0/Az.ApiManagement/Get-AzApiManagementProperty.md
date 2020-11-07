---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProperty.md
ms.openlocfilehash: 2c8fc24d252fce12e7adf9ee824db0e1b2c8b206
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676056"
---
# <span data-ttu-id="c1695-101">Get-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="c1695-101">Get-AzApiManagementProperty</span></span>

## <span data-ttu-id="c1695-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c1695-102">SYNOPSIS</span></span>
<span data-ttu-id="c1695-103">Ottiene un elenco o una proprietà specifica (nome-valore).</span><span class="sxs-lookup"><span data-stu-id="c1695-103">Gets a list or a particular Property (Named-Value).</span></span>

## <span data-ttu-id="c1695-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c1695-104">SYNTAX</span></span>

### <span data-ttu-id="c1695-105">GetAllProperties (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c1695-105">GetAllProperties (Default)</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c1695-106">GetByPropertyId</span><span class="sxs-lookup"><span data-stu-id="c1695-106">GetByPropertyId</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1695-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="c1695-107">GetByName</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1695-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="c1695-108">GetByTag</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1695-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1695-109">DESCRIPTION</span></span>
<span data-ttu-id="c1695-110">Il cmdlet **Get-AzApiManagementProperty** ottiene un elenco o una specifica proprietà.</span><span class="sxs-lookup"><span data-stu-id="c1695-110">The **Get-AzApiManagementProperty** cmdlet gets a list or a particular property.</span></span>

## <span data-ttu-id="c1695-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c1695-111">EXAMPLES</span></span>

### <span data-ttu-id="c1695-112">Esempio 1: ottenere la proprietà per nome</span><span class="sxs-lookup"><span data-stu-id="c1695-112">Example 1: Get Property by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProperty -Context $apimContext -Name "sql-connectionstring"
```

## <span data-ttu-id="c1695-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c1695-113">PARAMETERS</span></span>

### <span data-ttu-id="c1695-114">-Contesto</span><span class="sxs-lookup"><span data-stu-id="c1695-114">-Context</span></span>
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

### <span data-ttu-id="c1695-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1695-115">-DefaultProfile</span></span>
<span data-ttu-id="c1695-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c1695-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1695-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="c1695-117">-Name</span></span>
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

### <span data-ttu-id="c1695-118">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="c1695-118">-PropertyId</span></span>
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

### <span data-ttu-id="c1695-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="c1695-119">-Tag</span></span>
<span data-ttu-id="c1695-120">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="c1695-120">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c1695-121">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="c1695-121">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c1695-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1695-122">CommonParameters</span></span>
<span data-ttu-id="c1695-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1695-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1695-124">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1695-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1695-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c1695-125">INPUTS</span></span>

### <span data-ttu-id="c1695-126">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c1695-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c1695-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c1695-127">System.String</span></span>

## <span data-ttu-id="c1695-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c1695-128">OUTPUTS</span></span>

### <span data-ttu-id="c1695-129">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="c1695-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="c1695-130">Note</span><span class="sxs-lookup"><span data-stu-id="c1695-130">NOTES</span></span>

## <span data-ttu-id="c1695-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c1695-131">RELATED LINKS</span></span>

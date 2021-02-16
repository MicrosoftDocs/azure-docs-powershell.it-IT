---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementresourcelocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
ms.openlocfilehash: 505264809b513ad144fa3812193fc39f86ab9b1e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205658"
---
# <span data-ttu-id="35c3f-101">New-AzApiManagementResourceLocationObject</span><span class="sxs-lookup"><span data-stu-id="35c3f-101">New-AzApiManagementResourceLocationObject</span></span>

## <span data-ttu-id="35c3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35c3f-102">SYNOPSIS</span></span>
<span data-ttu-id="35c3f-103">Creare un nuovo contratto per la posizione delle risorse (usato in Gateway).</span><span class="sxs-lookup"><span data-stu-id="35c3f-103">Create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="35c3f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35c3f-104">SYNTAX</span></span>

```
New-AzApiManagementResourceLocationObject -Name <String> [-City <String>] [-District <String>]
 [-CountryOrRegion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35c3f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="35c3f-105">DESCRIPTION</span></span>
<span data-ttu-id="35c3f-106">Il cmdlet **New-AzApiManagementResourceLocationObject** crea un nuovo contratto per la posizione delle risorse (usato nei gateway).</span><span class="sxs-lookup"><span data-stu-id="35c3f-106">The **New-AzApiManagementResourceLocationObject** cmdlet create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="35c3f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35c3f-107">EXAMPLES</span></span>

### <span data-ttu-id="35c3f-108">Esempio 1: Creare un contratto per la posizione di una risorsa</span><span class="sxs-lookup"><span data-stu-id="35c3f-108">Example 1: Create a resource location contract</span></span>
```powershell
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
```

<span data-ttu-id="35c3f-109">Questo comando crea una posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="35c3f-109">This command creates a resource location.</span></span>

## <span data-ttu-id="35c3f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35c3f-110">PARAMETERS</span></span>

### <span data-ttu-id="35c3f-111">-Città</span><span class="sxs-lookup"><span data-stu-id="35c3f-111">-City</span></span>
<span data-ttu-id="35c3f-112">Città della località.</span><span class="sxs-lookup"><span data-stu-id="35c3f-112">Location City.</span></span>
<span data-ttu-id="35c3f-113">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="35c3f-113">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35c3f-114">-CountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="35c3f-114">-CountryOrRegion</span></span>
<span data-ttu-id="35c3f-115">Paese o area geografica della posizione.</span><span class="sxs-lookup"><span data-stu-id="35c3f-115">Location Country or Region.</span></span>
<span data-ttu-id="35c3f-116">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="35c3f-116">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35c3f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35c3f-117">-DefaultProfile</span></span>
<span data-ttu-id="35c3f-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="35c3f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35c3f-119">-District</span><span class="sxs-lookup"><span data-stu-id="35c3f-119">-District</span></span>
<span data-ttu-id="35c3f-120">Distretto delle località.</span><span class="sxs-lookup"><span data-stu-id="35c3f-120">Location District.</span></span>
<span data-ttu-id="35c3f-121">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="35c3f-121">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35c3f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="35c3f-122">-Name</span></span>
<span data-ttu-id="35c3f-123">Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="35c3f-123">Location Name.</span></span>
<span data-ttu-id="35c3f-124">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="35c3f-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35c3f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35c3f-125">CommonParameters</span></span>
<span data-ttu-id="35c3f-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35c3f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35c3f-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="35c3f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35c3f-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="35c3f-128">INPUTS</span></span>

### <span data-ttu-id="35c3f-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="35c3f-129">None</span></span>

## <span data-ttu-id="35c3f-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35c3f-130">OUTPUTS</span></span>

### <span data-ttu-id="35c3f-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="35c3f-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="35c3f-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="35c3f-132">NOTES</span></span>

## <span data-ttu-id="35c3f-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35c3f-133">RELATED LINKS</span></span>

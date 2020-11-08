---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementresourcelocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
ms.openlocfilehash: 505264809b513ad144fa3812193fc39f86ab9b1e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200556"
---
# <span data-ttu-id="baff9-101">New-AzApiManagementResourceLocationObject</span><span class="sxs-lookup"><span data-stu-id="baff9-101">New-AzApiManagementResourceLocationObject</span></span>

## <span data-ttu-id="baff9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="baff9-102">SYNOPSIS</span></span>
<span data-ttu-id="baff9-103">Creare un nuovo contratto per la posizione delle risorse (usato nei gateway).</span><span class="sxs-lookup"><span data-stu-id="baff9-103">Create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="baff9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="baff9-104">SYNTAX</span></span>

```
New-AzApiManagementResourceLocationObject -Name <String> [-City <String>] [-District <String>]
 [-CountryOrRegion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="baff9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="baff9-105">DESCRIPTION</span></span>
<span data-ttu-id="baff9-106">Il cmdlet **New-AzApiManagementResourceLocationObject** crea un nuovo contratto per la posizione delle risorse (usato nei gateway).</span><span class="sxs-lookup"><span data-stu-id="baff9-106">The **New-AzApiManagementResourceLocationObject** cmdlet create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="baff9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="baff9-107">EXAMPLES</span></span>

### <span data-ttu-id="baff9-108">Esempio 1: creare un contratto per la posizione delle risorse</span><span class="sxs-lookup"><span data-stu-id="baff9-108">Example 1: Create a resource location contract</span></span>
```powershell
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
```

<span data-ttu-id="baff9-109">Questo comando crea un percorso di risorsa.</span><span class="sxs-lookup"><span data-stu-id="baff9-109">This command creates a resource location.</span></span>

## <span data-ttu-id="baff9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="baff9-110">PARAMETERS</span></span>

### <span data-ttu-id="baff9-111">-Città</span><span class="sxs-lookup"><span data-stu-id="baff9-111">-City</span></span>
<span data-ttu-id="baff9-112">Città della posizione.</span><span class="sxs-lookup"><span data-stu-id="baff9-112">Location City.</span></span>
<span data-ttu-id="baff9-113">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="baff9-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="baff9-114">-CountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="baff9-114">-CountryOrRegion</span></span>
<span data-ttu-id="baff9-115">Paese o area geografica.</span><span class="sxs-lookup"><span data-stu-id="baff9-115">Location Country or Region.</span></span>
<span data-ttu-id="baff9-116">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="baff9-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="baff9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baff9-117">-DefaultProfile</span></span>
<span data-ttu-id="baff9-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="baff9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="baff9-119">-Distretto</span><span class="sxs-lookup"><span data-stu-id="baff9-119">-District</span></span>
<span data-ttu-id="baff9-120">Area geografica.</span><span class="sxs-lookup"><span data-stu-id="baff9-120">Location District.</span></span>
<span data-ttu-id="baff9-121">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="baff9-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="baff9-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="baff9-122">-Name</span></span>
<span data-ttu-id="baff9-123">Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="baff9-123">Location Name.</span></span>
<span data-ttu-id="baff9-124">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="baff9-124">This parameter is required.</span></span>

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

### <span data-ttu-id="baff9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baff9-125">CommonParameters</span></span>
<span data-ttu-id="baff9-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baff9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baff9-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="baff9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baff9-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="baff9-128">INPUTS</span></span>

### <span data-ttu-id="baff9-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="baff9-129">None</span></span>

## <span data-ttu-id="baff9-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="baff9-130">OUTPUTS</span></span>

### <span data-ttu-id="baff9-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="baff9-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="baff9-132">Note</span><span class="sxs-lookup"><span data-stu-id="baff9-132">NOTES</span></span>

## <span data-ttu-id="baff9-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="baff9-133">RELATED LINKS</span></span>

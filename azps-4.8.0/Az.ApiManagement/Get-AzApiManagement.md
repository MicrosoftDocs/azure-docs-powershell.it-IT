---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
ms.openlocfilehash: 41f7b921cb1977d7410c511be224b7e24623597b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192174"
---
# <span data-ttu-id="cd040-101">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd040-101">Get-AzApiManagement</span></span>

## <span data-ttu-id="cd040-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cd040-102">SYNOPSIS</span></span>
<span data-ttu-id="cd040-103">Ottiene un elenco o una particolare descrizione del servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="cd040-103">Gets a list or a particular API Management Service description.</span></span>

## <span data-ttu-id="cd040-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd040-104">SYNTAX</span></span>

### <span data-ttu-id="cd040-105">GetBySubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cd040-105">GetBySubscription (Default)</span></span>
```
Get-AzApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd040-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cd040-106">GetByResourceGroup</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd040-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="cd040-107">GetByResource</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cd040-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cd040-108">ByResourceId</span></span>
```
Get-AzApiManagement -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd040-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd040-109">DESCRIPTION</span></span>
<span data-ttu-id="cd040-110">Il cmdlet **Get-AzApiManagement** ottiene un elenco di tutti i servizi di gestione delle API in abbonamento o in un gruppo di risorse specificato o in una particolare gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="cd040-110">The **Get-AzApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="cd040-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd040-111">EXAMPLES</span></span>

### <span data-ttu-id="cd040-112">Esempio 1: ottenere tutti i servizi di gestione delle API</span><span class="sxs-lookup"><span data-stu-id="cd040-112">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzApiManagement
```

<span data-ttu-id="cd040-113">Questo comando consente di ottenere tutti i servizi di gestione delle API all'interno di un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="cd040-113">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="cd040-114">Esempio 2: ottenere tutti i servizi di gestione delle API in base a un nome specifico</span><span class="sxs-lookup"><span data-stu-id="cd040-114">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="cd040-115">Questo comando ottiene tutto il servizio di gestione delle API per nome.</span><span class="sxs-lookup"><span data-stu-id="cd040-115">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="cd040-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cd040-116">PARAMETERS</span></span>

### <span data-ttu-id="cd040-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd040-117">-DefaultProfile</span></span>
<span data-ttu-id="cd040-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cd040-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd040-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="cd040-119">-Name</span></span>
<span data-ttu-id="cd040-120">Specifica il nome del servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="cd040-120">Specifies the name of API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd040-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd040-121">-ResourceGroupName</span></span>
<span data-ttu-id="cd040-122">Specifica il nome del gruppo di risorse in cui questo cmdlet ottiene il servizio di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="cd040-122">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup, GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd040-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd040-123">-ResourceId</span></span>
<span data-ttu-id="cd040-124">ARM ResourceId del servizio di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="cd040-124">Arm ResourceId of the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd040-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd040-125">CommonParameters</span></span>
<span data-ttu-id="cd040-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd040-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd040-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd040-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd040-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cd040-128">INPUTS</span></span>

### <span data-ttu-id="cd040-129">System. String</span><span class="sxs-lookup"><span data-stu-id="cd040-129">System.String</span></span>

## <span data-ttu-id="cd040-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd040-130">OUTPUTS</span></span>

### <span data-ttu-id="cd040-131">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd040-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="cd040-132">Note</span><span class="sxs-lookup"><span data-stu-id="cd040-132">NOTES</span></span>

## <span data-ttu-id="cd040-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd040-133">RELATED LINKS</span></span>

[<span data-ttu-id="cd040-134">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd040-134">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="cd040-135">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd040-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="cd040-136">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd040-136">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="cd040-137">Ripristinare-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd040-137">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


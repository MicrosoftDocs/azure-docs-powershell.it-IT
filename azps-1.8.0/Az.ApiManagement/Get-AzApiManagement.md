---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
ms.openlocfilehash: c636da952c02b4f2b4795cd1703c276a23a8221c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673660"
---
# <span data-ttu-id="343d1-101">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="343d1-101">Get-AzApiManagement</span></span>

## <span data-ttu-id="343d1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="343d1-102">SYNOPSIS</span></span>
<span data-ttu-id="343d1-103">Ottiene un elenco o una particolare descrizione del servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="343d1-103">Gets a list or a particular API Management Service description.</span></span>

## <span data-ttu-id="343d1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="343d1-104">SYNTAX</span></span>

### <span data-ttu-id="343d1-105">GetBySubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="343d1-105">GetBySubscription (Default)</span></span>
```
Get-AzApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="343d1-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="343d1-106">GetByResourceGroup</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="343d1-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="343d1-107">GetByResource</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="343d1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="343d1-108">DESCRIPTION</span></span>
<span data-ttu-id="343d1-109">Il cmdlet **Get-AzApiManagement** ottiene un elenco di tutti i servizi di gestione delle API in abbonamento o in un gruppo di risorse specificato o in una particolare gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="343d1-109">The **Get-AzApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="343d1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="343d1-110">EXAMPLES</span></span>

### <span data-ttu-id="343d1-111">Esempio 1: ottenere tutti i servizi di gestione delle API</span><span class="sxs-lookup"><span data-stu-id="343d1-111">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzApiManagement
```

<span data-ttu-id="343d1-112">Questo comando consente di ottenere tutti i servizi di gestione delle API all'interno di un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="343d1-112">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="343d1-113">Esempio 2: ottenere tutti i servizi di gestione delle API in base a un nome specifico</span><span class="sxs-lookup"><span data-stu-id="343d1-113">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="343d1-114">Questo comando ottiene tutto il servizio di gestione delle API per nome.</span><span class="sxs-lookup"><span data-stu-id="343d1-114">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="343d1-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="343d1-115">PARAMETERS</span></span>

### <span data-ttu-id="343d1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="343d1-116">-DefaultProfile</span></span>
<span data-ttu-id="343d1-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="343d1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="343d1-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="343d1-118">-Name</span></span>
<span data-ttu-id="343d1-119">Specifica il nome del servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="343d1-119">Specifies the name of API Management service.</span></span>

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

### <span data-ttu-id="343d1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="343d1-120">-ResourceGroupName</span></span>
<span data-ttu-id="343d1-121">Specifica il nome del gruppo di risorse in cui questo cmdlet ottiene il servizio di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="343d1-121">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

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

### <span data-ttu-id="343d1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="343d1-122">CommonParameters</span></span>
<span data-ttu-id="343d1-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="343d1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="343d1-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="343d1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="343d1-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="343d1-125">INPUTS</span></span>

### <span data-ttu-id="343d1-126">System. String</span><span class="sxs-lookup"><span data-stu-id="343d1-126">System.String</span></span>

## <span data-ttu-id="343d1-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="343d1-127">OUTPUTS</span></span>

### <span data-ttu-id="343d1-128">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="343d1-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="343d1-129">Note</span><span class="sxs-lookup"><span data-stu-id="343d1-129">NOTES</span></span>

## <span data-ttu-id="343d1-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="343d1-130">RELATED LINKS</span></span>

[<span data-ttu-id="343d1-131">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="343d1-131">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="343d1-132">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="343d1-132">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="343d1-133">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="343d1-133">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="343d1-134">Ripristinare-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="343d1-134">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)



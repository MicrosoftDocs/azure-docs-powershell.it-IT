---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
ms.openlocfilehash: 610f8589dbb6c01cae1a3eb37f886425a3664929
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508851"
---
# <span data-ttu-id="8578c-101">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="8578c-101">Get-AzureRmApiManagement</span></span>

## <span data-ttu-id="8578c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8578c-102">SYNOPSIS</span></span>
<span data-ttu-id="8578c-103">Ottiene un elenco o una particolare descrizione del servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="8578c-103">Gets a list or a particular API Management Service description.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8578c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8578c-104">SYNTAX</span></span>

### <span data-ttu-id="8578c-105">Tutti in abbonamento (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8578c-105">All In Subscription (Default)</span></span>
```
Get-AzureRmApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8578c-106">Tutti nel gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="8578c-106">All In Resource Group</span></span>
```
Get-AzureRmApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8578c-107">Servizio di gestione API specifico</span><span class="sxs-lookup"><span data-stu-id="8578c-107">Specific API Management Service</span></span>
```
Get-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8578c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8578c-108">DESCRIPTION</span></span>
<span data-ttu-id="8578c-109">Il cmdlet **Get-AzureRmApiManagement** ottiene un elenco di tutti i servizi di gestione delle API in abbonamento o in un gruppo di risorse specificato o in una particolare gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="8578c-109">The **Get-AzureRmApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="8578c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8578c-110">EXAMPLES</span></span>

### <span data-ttu-id="8578c-111">Esempio 1: ottenere tutti i servizi di gestione delle API</span><span class="sxs-lookup"><span data-stu-id="8578c-111">Example 1: Get all API Management services</span></span>
```
PS C:\>Get-AzureRmApiManagement
```

<span data-ttu-id="8578c-112">Questo comando consente di ottenere tutti i servizi di gestione delle API all'interno di un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="8578c-112">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="8578c-113">Esempio 2: ottenere tutti i servizi di gestione delle API in base a un nome specifico</span><span class="sxs-lookup"><span data-stu-id="8578c-113">Example 2: Get all API Management services by a specific name</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="8578c-114">Questo comando ottiene tutto il servizio di gestione delle API per nome.</span><span class="sxs-lookup"><span data-stu-id="8578c-114">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="8578c-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8578c-115">PARAMETERS</span></span>

### <span data-ttu-id="8578c-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="8578c-116">-Name</span></span>
<span data-ttu-id="8578c-117">Specifica il nome del servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="8578c-117">Specifies the name of API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8578c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8578c-118">-ResourceGroupName</span></span>
<span data-ttu-id="8578c-119">Specifica il nome del gruppo di risorse in cui questo cmdlet ottiene il servizio di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="8578c-119">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group, Specific API Management Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8578c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8578c-120">-DefaultProfile</span></span>
<span data-ttu-id="8578c-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8578c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8578c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8578c-122">CommonParameters</span></span>
<span data-ttu-id="8578c-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8578c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8578c-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8578c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8578c-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8578c-125">INPUTS</span></span>

## <span data-ttu-id="8578c-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8578c-126">OUTPUTS</span></span>

### <span data-ttu-id="8578c-127">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement]</span><span class="sxs-lookup"><span data-stu-id="8578c-127">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement]</span></span>

## <span data-ttu-id="8578c-128">Note</span><span class="sxs-lookup"><span data-stu-id="8578c-128">NOTES</span></span>

## <span data-ttu-id="8578c-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8578c-129">RELATED LINKS</span></span>

[<span data-ttu-id="8578c-130">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="8578c-130">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="8578c-131">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="8578c-131">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="8578c-132">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="8578c-132">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="8578c-133">Ripristinare-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="8578c-133">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)



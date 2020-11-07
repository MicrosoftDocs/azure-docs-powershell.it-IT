---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebApp.md
ms.openlocfilehash: 64945cf503248fc0561dc894090c73d2d7151e4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686538"
---
# <span data-ttu-id="660d9-101">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="660d9-101">Get-AzureRmWebApp</span></span>

## <span data-ttu-id="660d9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="660d9-102">SYNOPSIS</span></span>
<span data-ttu-id="660d9-103">Ottiene le app Web di Azure nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="660d9-103">Gets Azure Web Apps in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="660d9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="660d9-104">SYNTAX</span></span>

### <span data-ttu-id="660d9-105">S1</span><span class="sxs-lookup"><span data-stu-id="660d9-105">S1</span></span>
```
Get-AzureRmWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="660d9-106">S2</span><span class="sxs-lookup"><span data-stu-id="660d9-106">S2</span></span>
```
Get-AzureRmWebApp [-AppServicePlan] <ServerFarmWithRichSku> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="660d9-107">S3</span><span class="sxs-lookup"><span data-stu-id="660d9-107">S3</span></span>
```
Get-AzureRmWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="660d9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="660d9-108">DESCRIPTION</span></span>
<span data-ttu-id="660d9-109">Il cmdlet **Get-AzureRmWebApp** ottiene le informazioni su un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="660d9-109">The **Get-AzureRmWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="660d9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="660d9-110">EXAMPLES</span></span>

### <span data-ttu-id="660d9-111">Esempio 1: ottenere un'app Web da un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="660d9-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -SlotName "Slot001"
```

<span data-ttu-id="660d9-112">Questo comando consente di ottenere l'app Web denominata ContosoSite che appartiene al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="660d9-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="660d9-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="660d9-113">PARAMETERS</span></span>

### <span data-ttu-id="660d9-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="660d9-114">-AppServicePlan</span></span>
<span data-ttu-id="660d9-115">Oggetto piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="660d9-115">App Service Plan object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="660d9-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="660d9-116">-Location</span></span>
<span data-ttu-id="660d9-117">Posizione</span><span class="sxs-lookup"><span data-stu-id="660d9-117">Location</span></span>

```yaml
Type: System.String
Parameter Sets: S3
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="660d9-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="660d9-118">-Name</span></span>
<span data-ttu-id="660d9-119">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="660d9-119">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="660d9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="660d9-120">-ResourceGroupName</span></span>
<span data-ttu-id="660d9-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="660d9-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="660d9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="660d9-122">-DefaultProfile</span></span>
<span data-ttu-id="660d9-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="660d9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="660d9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="660d9-124">CommonParameters</span></span>
<span data-ttu-id="660d9-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="660d9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="660d9-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="660d9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="660d9-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="660d9-127">INPUTS</span></span>

## <span data-ttu-id="660d9-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="660d9-128">OUTPUTS</span></span>

## <span data-ttu-id="660d9-129">Note</span><span class="sxs-lookup"><span data-stu-id="660d9-129">NOTES</span></span>

## <span data-ttu-id="660d9-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="660d9-130">RELATED LINKS</span></span>

[<span data-ttu-id="660d9-131">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="660d9-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="660d9-132">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="660d9-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="660d9-133">Riavviare-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="660d9-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="660d9-134">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="660d9-134">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="660d9-135">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="660d9-135">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)



---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: eb1f96eaf85e6a5e7234e09c319b2e0c1117d456
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865714"
---
# <span data-ttu-id="49fff-101">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="49fff-101">Get-AzureRmWebApp</span></span>

## <span data-ttu-id="49fff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="49fff-102">SYNOPSIS</span></span>
<span data-ttu-id="49fff-103">Ottiene le app Web di Azure nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="49fff-103">Gets Azure Web Apps in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49fff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49fff-104">SYNTAX</span></span>

### <span data-ttu-id="49fff-105">S1</span><span class="sxs-lookup"><span data-stu-id="49fff-105">S1</span></span>
```
Get-AzureRmWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="49fff-106">S2</span><span class="sxs-lookup"><span data-stu-id="49fff-106">S2</span></span>
```
Get-AzureRmWebApp [-AppServicePlan] <AppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="49fff-107">S3</span><span class="sxs-lookup"><span data-stu-id="49fff-107">S3</span></span>
```
Get-AzureRmWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49fff-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49fff-108">DESCRIPTION</span></span>
<span data-ttu-id="49fff-109">Il cmdlet **Get-AzureRmWebApp** ottiene le informazioni su un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="49fff-109">The **Get-AzureRmWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="49fff-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49fff-110">EXAMPLES</span></span>

### <span data-ttu-id="49fff-111">Esempio 1: ottenere un'app Web da un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="49fff-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="49fff-112">Questo comando consente di ottenere l'app Web denominata ContosoSite che appartiene al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="49fff-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="49fff-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="49fff-113">PARAMETERS</span></span>

### <span data-ttu-id="49fff-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="49fff-114">-AppServicePlan</span></span>
<span data-ttu-id="49fff-115">Oggetto piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="49fff-115">App Service Plan object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49fff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49fff-116">-DefaultProfile</span></span>
<span data-ttu-id="49fff-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="49fff-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49fff-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="49fff-118">-Location</span></span>
<span data-ttu-id="49fff-119">Posizione</span><span class="sxs-lookup"><span data-stu-id="49fff-119">Location</span></span>

```yaml
Type: String
Parameter Sets: S3
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49fff-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="49fff-120">-Name</span></span>
<span data-ttu-id="49fff-121">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="49fff-121">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49fff-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49fff-122">-ResourceGroupName</span></span>
<span data-ttu-id="49fff-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="49fff-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49fff-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49fff-124">CommonParameters</span></span>
<span data-ttu-id="49fff-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49fff-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49fff-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49fff-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49fff-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="49fff-127">INPUTS</span></span>

### <span data-ttu-id="49fff-128">System. String</span><span class="sxs-lookup"><span data-stu-id="49fff-128">System.String</span></span>

## <span data-ttu-id="49fff-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49fff-129">OUTPUTS</span></span>

### <span data-ttu-id="49fff-130">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="49fff-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="49fff-131">Note</span><span class="sxs-lookup"><span data-stu-id="49fff-131">NOTES</span></span>

## <span data-ttu-id="49fff-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49fff-132">RELATED LINKS</span></span>

[<span data-ttu-id="49fff-133">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="49fff-133">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="49fff-134">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="49fff-134">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="49fff-135">Riavviare-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="49fff-135">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="49fff-136">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="49fff-136">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="49fff-137">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="49fff-137">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)



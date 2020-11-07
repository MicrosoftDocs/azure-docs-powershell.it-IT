---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
ms.openlocfilehash: d1217f3abc00fec8752fcddbb30e577df087b5de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676324"
---
# <span data-ttu-id="bed92-101">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="bed92-101">Get-AzWebApp</span></span>

## <span data-ttu-id="bed92-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bed92-102">SYNOPSIS</span></span>
<span data-ttu-id="bed92-103">Ottiene le app Web di Azure nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="bed92-103">Gets Azure Web Apps in the specified resource group.</span></span>

## <span data-ttu-id="bed92-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bed92-104">SYNTAX</span></span>

### <span data-ttu-id="bed92-105">S1</span><span class="sxs-lookup"><span data-stu-id="bed92-105">S1</span></span>
```
Get-AzWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bed92-106">S2</span><span class="sxs-lookup"><span data-stu-id="bed92-106">S2</span></span>
```
Get-AzWebApp [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bed92-107">S3</span><span class="sxs-lookup"><span data-stu-id="bed92-107">S3</span></span>
```
Get-AzWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bed92-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bed92-108">DESCRIPTION</span></span>
<span data-ttu-id="bed92-109">Il cmdlet **Get-AzWebApp** ottiene le informazioni su un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="bed92-109">The **Get-AzWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="bed92-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bed92-110">EXAMPLES</span></span>

### <span data-ttu-id="bed92-111">Esempio 1: ottenere un'app Web da un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="bed92-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="bed92-112">Questo comando consente di ottenere l'app Web denominata ContosoSite che appartiene al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="bed92-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="bed92-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bed92-113">PARAMETERS</span></span>

### <span data-ttu-id="bed92-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bed92-114">-AppServicePlan</span></span>
<span data-ttu-id="bed92-115">Oggetto piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="bed92-115">App Service Plan object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bed92-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bed92-116">-DefaultProfile</span></span>
<span data-ttu-id="bed92-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bed92-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bed92-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="bed92-118">-Location</span></span>
<span data-ttu-id="bed92-119">Posizione</span><span class="sxs-lookup"><span data-stu-id="bed92-119">Location</span></span>

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

### <span data-ttu-id="bed92-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="bed92-120">-Name</span></span>
<span data-ttu-id="bed92-121">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="bed92-121">WebApp Name</span></span>

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

### <span data-ttu-id="bed92-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bed92-122">-ResourceGroupName</span></span>
<span data-ttu-id="bed92-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="bed92-123">Resource Group Name</span></span>

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

### <span data-ttu-id="bed92-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bed92-124">CommonParameters</span></span>
<span data-ttu-id="bed92-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bed92-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bed92-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bed92-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bed92-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bed92-127">INPUTS</span></span>

### <span data-ttu-id="bed92-128">System. String</span><span class="sxs-lookup"><span data-stu-id="bed92-128">System.String</span></span>

## <span data-ttu-id="bed92-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bed92-129">OUTPUTS</span></span>

### <span data-ttu-id="bed92-130">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="bed92-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="bed92-131">Note</span><span class="sxs-lookup"><span data-stu-id="bed92-131">NOTES</span></span>

## <span data-ttu-id="bed92-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bed92-132">RELATED LINKS</span></span>

[<span data-ttu-id="bed92-133">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="bed92-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="bed92-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="bed92-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="bed92-135">Riavviare-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="bed92-135">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="bed92-136">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="bed92-136">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="bed92-137">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="bed92-137">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
ms.openlocfilehash: 7dc1d2c5d6be1fd920ec9fb4eb90bf73b2c464b9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326953"
---
# <span data-ttu-id="8bc1b-101">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8bc1b-101">Get-AzWebApp</span></span>

## <span data-ttu-id="8bc1b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8bc1b-102">SYNOPSIS</span></span>
<span data-ttu-id="8bc1b-103">Ottiene le app Web di Azure nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="8bc1b-103">Gets Azure Web Apps in the specified resource group.</span></span>

## <span data-ttu-id="8bc1b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8bc1b-104">SYNTAX</span></span>

### <span data-ttu-id="8bc1b-105">S1</span><span class="sxs-lookup"><span data-stu-id="8bc1b-105">S1</span></span>
```
Get-AzWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8bc1b-106">S2</span><span class="sxs-lookup"><span data-stu-id="8bc1b-106">S2</span></span>
```
Get-AzWebApp [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8bc1b-107">S3</span><span class="sxs-lookup"><span data-stu-id="8bc1b-107">S3</span></span>
```
Get-AzWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8bc1b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8bc1b-108">DESCRIPTION</span></span>
<span data-ttu-id="8bc1b-109">Il cmdlet **Get-AzWebApp** ottiene le informazioni su un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="8bc1b-109">The **Get-AzWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="8bc1b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8bc1b-110">EXAMPLES</span></span>

### <span data-ttu-id="8bc1b-111">Esempio 1: ottenere un'app Web da un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="8bc1b-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="8bc1b-112">Questo comando consente di ottenere l'app Web denominata ContosoSite che appartiene al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="8bc1b-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="8bc1b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8bc1b-113">PARAMETERS</span></span>

### <span data-ttu-id="8bc1b-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8bc1b-114">-AppServicePlan</span></span>
<span data-ttu-id="8bc1b-115">Oggetto piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="8bc1b-115">App Service Plan object</span></span>

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

### <span data-ttu-id="8bc1b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bc1b-116">-DefaultProfile</span></span>
<span data-ttu-id="8bc1b-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8bc1b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8bc1b-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="8bc1b-118">-Location</span></span>
<span data-ttu-id="8bc1b-119">Posizione</span><span class="sxs-lookup"><span data-stu-id="8bc1b-119">Location</span></span>

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

### <span data-ttu-id="8bc1b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="8bc1b-120">-Name</span></span>
<span data-ttu-id="8bc1b-121">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="8bc1b-121">WebApp Name</span></span>

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

### <span data-ttu-id="8bc1b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bc1b-122">-ResourceGroupName</span></span>
<span data-ttu-id="8bc1b-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="8bc1b-123">Resource Group Name</span></span>

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

### <span data-ttu-id="8bc1b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bc1b-124">CommonParameters</span></span>
<span data-ttu-id="8bc1b-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bc1b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bc1b-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bc1b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bc1b-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8bc1b-127">INPUTS</span></span>

### <span data-ttu-id="8bc1b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8bc1b-128">System.String</span></span>

## <span data-ttu-id="8bc1b-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8bc1b-129">OUTPUTS</span></span>

### <span data-ttu-id="8bc1b-130">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="8bc1b-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8bc1b-131">Note</span><span class="sxs-lookup"><span data-stu-id="8bc1b-131">NOTES</span></span>

## <span data-ttu-id="8bc1b-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8bc1b-132">RELATED LINKS</span></span>

[<span data-ttu-id="8bc1b-133">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8bc1b-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="8bc1b-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8bc1b-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="8bc1b-135">Riavviare-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8bc1b-135">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="8bc1b-136">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8bc1b-136">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="8bc1b-137">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8bc1b-137">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)



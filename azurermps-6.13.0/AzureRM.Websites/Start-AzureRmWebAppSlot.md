---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/start-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebAppSlot.md
ms.openlocfilehash: 089711bacd6401b4c44683a159e43a92a56106d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508912"
---
# <span data-ttu-id="ecbea-101">Start-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ecbea-101">Start-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="ecbea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ecbea-102">SYNOPSIS</span></span>
<span data-ttu-id="ecbea-103">Avvia uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ecbea-103">Starts an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecbea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ecbea-104">SYNTAX</span></span>

### <span data-ttu-id="ecbea-105">S1</span><span class="sxs-lookup"><span data-stu-id="ecbea-105">S1</span></span>
```
Start-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecbea-106">S2</span><span class="sxs-lookup"><span data-stu-id="ecbea-106">S2</span></span>
```
Start-AzureRmWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecbea-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ecbea-107">DESCRIPTION</span></span>
<span data-ttu-id="ecbea-108">Il cmdlet **Start-AzureRmWebAppSlot** avvia uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ecbea-108">The **Start-AzureRmWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="ecbea-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ecbea-109">EXAMPLES</span></span>

### <span data-ttu-id="ecbea-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ecbea-110">Example 1</span></span>
```
PS C:\>Start-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="ecbea-111">Questo comando avvia lo slot denominato Slot001 pertinente all'app Web denominata ContosoWebApp che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="ecbea-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="ecbea-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ecbea-112">PARAMETERS</span></span>

### <span data-ttu-id="ecbea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecbea-113">-DefaultProfile</span></span>
<span data-ttu-id="ecbea-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ecbea-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecbea-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ecbea-115">-Name</span></span>
<span data-ttu-id="ecbea-116">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="ecbea-116">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecbea-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecbea-117">-ResourceGroupName</span></span>
<span data-ttu-id="ecbea-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="ecbea-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecbea-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="ecbea-119">-Slot</span></span>
<span data-ttu-id="ecbea-120">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="ecbea-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecbea-121">-Web App</span><span class="sxs-lookup"><span data-stu-id="ecbea-121">-WebApp</span></span>
<span data-ttu-id="ecbea-122">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="ecbea-122">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecbea-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecbea-123">CommonParameters</span></span>
<span data-ttu-id="ecbea-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecbea-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecbea-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecbea-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecbea-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ecbea-126">INPUTS</span></span>

### <span data-ttu-id="ecbea-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ecbea-127">System.String</span></span>

### <span data-ttu-id="ecbea-128">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="ecbea-128">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="ecbea-129">Parametri: Web App (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ecbea-129">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="ecbea-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ecbea-130">OUTPUTS</span></span>

### <span data-ttu-id="ecbea-131">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="ecbea-131">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="ecbea-132">Note</span><span class="sxs-lookup"><span data-stu-id="ecbea-132">NOTES</span></span>

## <span data-ttu-id="ecbea-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ecbea-133">RELATED LINKS</span></span>

[<span data-ttu-id="ecbea-134">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ecbea-134">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="ecbea-135">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ecbea-135">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="ecbea-136">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ecbea-136">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="ecbea-137">Riavviare-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ecbea-137">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="ecbea-138">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ecbea-138">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="ecbea-139">Stop-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ecbea-139">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="ecbea-140">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ecbea-140">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

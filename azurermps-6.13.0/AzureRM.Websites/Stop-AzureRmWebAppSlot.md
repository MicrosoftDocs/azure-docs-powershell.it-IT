---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebAppSlot.md
ms.openlocfilehash: 2e6130b93a3c549ca84c2cb0a6a336f6afb177b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514720"
---
# <span data-ttu-id="ebca2-101">Stop-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ebca2-101">Stop-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="ebca2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ebca2-102">SYNOPSIS</span></span>
<span data-ttu-id="ebca2-103">Interrompe uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ebca2-103">Stops an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebca2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ebca2-104">SYNTAX</span></span>

### <span data-ttu-id="ebca2-105">S1</span><span class="sxs-lookup"><span data-stu-id="ebca2-105">S1</span></span>
```
Stop-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ebca2-106">S2</span><span class="sxs-lookup"><span data-stu-id="ebca2-106">S2</span></span>
```
Stop-AzureRmWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebca2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ebca2-107">DESCRIPTION</span></span>
<span data-ttu-id="ebca2-108">Il cmdlet **Stop-AzureRmWebAppSlot** arresta uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ebca2-108">The **Stop-AzureRmWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="ebca2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ebca2-109">EXAMPLES</span></span>

### <span data-ttu-id="ebca2-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ebca2-110">Example 1</span></span>
```
PS C:\>Stop-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="ebca2-111">Questo comando Arresta lo slot Slot001 pertinente all'app Web denominata ContosoWebApp che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="ebca2-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="ebca2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ebca2-112">PARAMETERS</span></span>

### <span data-ttu-id="ebca2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebca2-113">-DefaultProfile</span></span>
<span data-ttu-id="ebca2-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ebca2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebca2-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ebca2-115">-Name</span></span>
<span data-ttu-id="ebca2-116">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="ebca2-116">WebApp Name</span></span>

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

### <span data-ttu-id="ebca2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebca2-117">-ResourceGroupName</span></span>
<span data-ttu-id="ebca2-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="ebca2-118">Resource Group Name</span></span>

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

### <span data-ttu-id="ebca2-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="ebca2-119">-Slot</span></span>
<span data-ttu-id="ebca2-120">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="ebca2-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="ebca2-121">-Web App</span><span class="sxs-lookup"><span data-stu-id="ebca2-121">-WebApp</span></span>
<span data-ttu-id="ebca2-122">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="ebca2-122">WebApp Object</span></span>

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

### <span data-ttu-id="ebca2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebca2-123">CommonParameters</span></span>
<span data-ttu-id="ebca2-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebca2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebca2-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebca2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebca2-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ebca2-126">INPUTS</span></span>

### <span data-ttu-id="ebca2-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ebca2-127">System.String</span></span>

### <span data-ttu-id="ebca2-128">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="ebca2-128">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="ebca2-129">Parametri: Web App (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ebca2-129">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="ebca2-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ebca2-130">OUTPUTS</span></span>

### <span data-ttu-id="ebca2-131">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="ebca2-131">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="ebca2-132">Note</span><span class="sxs-lookup"><span data-stu-id="ebca2-132">NOTES</span></span>

## <span data-ttu-id="ebca2-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ebca2-133">RELATED LINKS</span></span>

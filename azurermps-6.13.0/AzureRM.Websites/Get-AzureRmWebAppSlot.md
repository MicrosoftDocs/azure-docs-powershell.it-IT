---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlot.md
ms.openlocfilehash: f7be5b7877362484d0f3dfe4d19b8afc669e917c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507251"
---
# <span data-ttu-id="45476-101">Get-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45476-101">Get-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="45476-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="45476-102">SYNOPSIS</span></span>
<span data-ttu-id="45476-103">Ottiene uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="45476-103">Gets an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45476-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="45476-104">SYNTAX</span></span>

### <span data-ttu-id="45476-105">S1</span><span class="sxs-lookup"><span data-stu-id="45476-105">S1</span></span>
```
Get-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45476-106">S2</span><span class="sxs-lookup"><span data-stu-id="45476-106">S2</span></span>
```
Get-AzureRmWebAppSlot [[-Slot] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="45476-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45476-107">DESCRIPTION</span></span>
<span data-ttu-id="45476-108">Il cmdlet **Get-AzureRmWebAppSlot** ottiene le informazioni su uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="45476-108">The **Get-AzureRmWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="45476-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="45476-109">EXAMPLES</span></span>

### <span data-ttu-id="45476-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="45476-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="45476-111">Questo comando ottiene lo slot denominato Slot001 dall'app Web denominata WebAppStandard che appartiene al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="45476-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="45476-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="45476-112">PARAMETERS</span></span>

### <span data-ttu-id="45476-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45476-113">-DefaultProfile</span></span>
<span data-ttu-id="45476-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="45476-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45476-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="45476-115">-Name</span></span>
<span data-ttu-id="45476-116">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="45476-116">WebApp Name</span></span>

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

### <span data-ttu-id="45476-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45476-117">-ResourceGroupName</span></span>
<span data-ttu-id="45476-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="45476-118">Resource Group Name</span></span>

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

### <span data-ttu-id="45476-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="45476-119">-Slot</span></span>
<span data-ttu-id="45476-120">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="45476-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45476-121">-Web App</span><span class="sxs-lookup"><span data-stu-id="45476-121">-WebApp</span></span>
<span data-ttu-id="45476-122">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="45476-122">WebApp Object</span></span>

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

### <span data-ttu-id="45476-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45476-123">CommonParameters</span></span>
<span data-ttu-id="45476-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45476-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45476-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45476-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45476-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="45476-126">INPUTS</span></span>

### <span data-ttu-id="45476-127">System. String</span><span class="sxs-lookup"><span data-stu-id="45476-127">System.String</span></span>

### <span data-ttu-id="45476-128">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="45476-128">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="45476-129">Parametri: Web App (ByValue)</span><span class="sxs-lookup"><span data-stu-id="45476-129">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="45476-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="45476-130">OUTPUTS</span></span>

### <span data-ttu-id="45476-131">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="45476-131">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="45476-132">Note</span><span class="sxs-lookup"><span data-stu-id="45476-132">NOTES</span></span>

## <span data-ttu-id="45476-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="45476-133">RELATED LINKS</span></span>

[<span data-ttu-id="45476-134">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45476-134">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="45476-135">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45476-135">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="45476-136">Riavviare-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45476-136">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="45476-137">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45476-137">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="45476-138">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45476-138">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="45476-139">Stop-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45476-139">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="45476-140">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="45476-140">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

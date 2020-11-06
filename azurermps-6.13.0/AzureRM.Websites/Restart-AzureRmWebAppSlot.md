---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restart-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebAppSlot.md
ms.openlocfilehash: 2d1c4fe635e6d4bc509f82f1af376ee0f662217a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516324"
---
# <span data-ttu-id="81a42-101">Restart-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="81a42-101">Restart-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="81a42-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="81a42-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81a42-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="81a42-103">SYNTAX</span></span>

### <span data-ttu-id="81a42-104">S1</span><span class="sxs-lookup"><span data-stu-id="81a42-104">S1</span></span>
```
Restart-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81a42-105">S2</span><span class="sxs-lookup"><span data-stu-id="81a42-105">S2</span></span>
```
Restart-AzureRmWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81a42-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81a42-106">DESCRIPTION</span></span>
<span data-ttu-id="81a42-107">Il cmdlet **Restart-AzureRmWebAppSlot** si arresta e quindi avvia uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="81a42-107">The **Restart-AzureRmWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="81a42-108">Se lo slot per l'app Web si trova in uno stato interrotto, usa il cmdlet Start-AzureRmWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="81a42-108">If the Web App Slot is in a stopped state, use the Start-AzureRmWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="81a42-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="81a42-109">EXAMPLES</span></span>

### <span data-ttu-id="81a42-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="81a42-110">Example 1</span></span>
```
PS C:\> Restart-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="81a42-111">Questo comando Riavvia lo slot Slot001 per l'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus</span><span class="sxs-lookup"><span data-stu-id="81a42-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="81a42-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="81a42-112">PARAMETERS</span></span>

### <span data-ttu-id="81a42-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81a42-113">-DefaultProfile</span></span>
<span data-ttu-id="81a42-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="81a42-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81a42-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="81a42-115">-Name</span></span>
<span data-ttu-id="81a42-116">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="81a42-116">WebApp Name</span></span>

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

### <span data-ttu-id="81a42-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81a42-117">-ResourceGroupName</span></span>
<span data-ttu-id="81a42-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="81a42-118">Resource Group Name</span></span>

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

### <span data-ttu-id="81a42-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="81a42-119">-Slot</span></span>
<span data-ttu-id="81a42-120">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="81a42-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="81a42-121">-Web App</span><span class="sxs-lookup"><span data-stu-id="81a42-121">-WebApp</span></span>
<span data-ttu-id="81a42-122">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="81a42-122">WebApp Object</span></span>

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

### <span data-ttu-id="81a42-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81a42-123">CommonParameters</span></span>
<span data-ttu-id="81a42-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81a42-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81a42-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81a42-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81a42-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="81a42-126">INPUTS</span></span>

### <span data-ttu-id="81a42-127">System. String</span><span class="sxs-lookup"><span data-stu-id="81a42-127">System.String</span></span>

### <span data-ttu-id="81a42-128">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="81a42-128">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="81a42-129">Parametri: Web App (ByValue)</span><span class="sxs-lookup"><span data-stu-id="81a42-129">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="81a42-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="81a42-130">OUTPUTS</span></span>

### <span data-ttu-id="81a42-131">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="81a42-131">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="81a42-132">Note</span><span class="sxs-lookup"><span data-stu-id="81a42-132">NOTES</span></span>

## <span data-ttu-id="81a42-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="81a42-133">RELATED LINKS</span></span>

[<span data-ttu-id="81a42-134">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="81a42-134">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="81a42-135">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="81a42-135">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="81a42-136">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="81a42-136">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="81a42-137">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="81a42-137">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="81a42-138">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="81a42-138">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="81a42-139">Stop-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="81a42-139">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="81a42-140">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="81a42-140">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

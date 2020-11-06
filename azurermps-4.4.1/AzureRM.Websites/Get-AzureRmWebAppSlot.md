---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlot.md
ms.openlocfilehash: 841cc1f8356d9b082dec55e689033c19343041d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512776"
---
# <span data-ttu-id="d3dc8-101">Get-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d3dc8-101">Get-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="d3dc8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3dc8-102">SYNOPSIS</span></span>
<span data-ttu-id="d3dc8-103">Ottiene uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="d3dc8-103">Gets an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3dc8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3dc8-104">SYNTAX</span></span>

### <span data-ttu-id="d3dc8-105">S1</span><span class="sxs-lookup"><span data-stu-id="d3dc8-105">S1</span></span>
```
Get-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3dc8-106">S2</span><span class="sxs-lookup"><span data-stu-id="d3dc8-106">S2</span></span>
```
Get-AzureRmWebAppSlot [[-Slot] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d3dc8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3dc8-107">DESCRIPTION</span></span>
<span data-ttu-id="d3dc8-108">Il cmdlet **Get-AzureRmWebAppSlot** ottiene le informazioni su uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="d3dc8-108">The **Get-AzureRmWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="d3dc8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3dc8-109">EXAMPLES</span></span>

### <span data-ttu-id="d3dc8-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d3dc8-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="d3dc8-111">Questo comando ottiene lo slot denominato Slot001 dall'app Web denominata WebAppStandard che appartiene al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="d3dc8-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="d3dc8-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3dc8-112">PARAMETERS</span></span>

### <span data-ttu-id="d3dc8-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="d3dc8-113">-Name</span></span>
<span data-ttu-id="d3dc8-114">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="d3dc8-114">WebApp Name</span></span>

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

### <span data-ttu-id="d3dc8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3dc8-115">-ResourceGroupName</span></span>
<span data-ttu-id="d3dc8-116">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="d3dc8-116">Resource Group Name</span></span>

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

### <span data-ttu-id="d3dc8-117">-Slot</span><span class="sxs-lookup"><span data-stu-id="d3dc8-117">-Slot</span></span>
<span data-ttu-id="d3dc8-118">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="d3dc8-118">WebApp Slot Name</span></span>

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

### <span data-ttu-id="d3dc8-119">-Web App</span><span class="sxs-lookup"><span data-stu-id="d3dc8-119">-WebApp</span></span>
<span data-ttu-id="d3dc8-120">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="d3dc8-120">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3dc8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3dc8-121">-DefaultProfile</span></span>
<span data-ttu-id="d3dc8-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3dc8-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3dc8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3dc8-123">CommonParameters</span></span>
<span data-ttu-id="d3dc8-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3dc8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3dc8-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3dc8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3dc8-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3dc8-126">INPUTS</span></span>

### <span data-ttu-id="d3dc8-127">Sito</span><span class="sxs-lookup"><span data-stu-id="d3dc8-127">Site</span></span>
<span data-ttu-id="d3dc8-128">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="d3dc8-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="d3dc8-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3dc8-129">OUTPUTS</span></span>

## <span data-ttu-id="d3dc8-130">Note</span><span class="sxs-lookup"><span data-stu-id="d3dc8-130">NOTES</span></span>

## <span data-ttu-id="d3dc8-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3dc8-131">RELATED LINKS</span></span>

[<span data-ttu-id="d3dc8-132">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d3dc8-132">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="d3dc8-133">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d3dc8-133">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="d3dc8-134">Riavviare-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d3dc8-134">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="d3dc8-135">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d3dc8-135">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="d3dc8-136">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d3dc8-136">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="d3dc8-137">Stop-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d3dc8-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="d3dc8-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="d3dc8-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

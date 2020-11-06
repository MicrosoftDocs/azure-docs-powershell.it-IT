---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebAppSlot.md
ms.openlocfilehash: 687adf3cd7101a9747346c4b1aa3ba201d6dcc46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508476"
---
# <span data-ttu-id="16e01-101">Start-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="16e01-101">Start-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="16e01-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="16e01-102">SYNOPSIS</span></span>
<span data-ttu-id="16e01-103">Avvia uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="16e01-103">Starts an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16e01-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="16e01-104">SYNTAX</span></span>

### <span data-ttu-id="16e01-105">S1</span><span class="sxs-lookup"><span data-stu-id="16e01-105">S1</span></span>
```
Start-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16e01-106">S2</span><span class="sxs-lookup"><span data-stu-id="16e01-106">S2</span></span>
```
Start-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16e01-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16e01-107">DESCRIPTION</span></span>
<span data-ttu-id="16e01-108">Il cmdlet **Start-AzureRmWebAppSlot** avvia uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="16e01-108">The **Start-AzureRmWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="16e01-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="16e01-109">EXAMPLES</span></span>

### <span data-ttu-id="16e01-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="16e01-110">Example 1</span></span>
```
PS C:\>Start-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="16e01-111">Questo comando avvia lo slot denominato Slot001 pertinente all'app Web denominata ContosoWebApp che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="16e01-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="16e01-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="16e01-112">PARAMETERS</span></span>

### <span data-ttu-id="16e01-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="16e01-113">-Name</span></span>
<span data-ttu-id="16e01-114">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="16e01-114">WebApp Name</span></span>

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

### <span data-ttu-id="16e01-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16e01-115">-ResourceGroupName</span></span>
<span data-ttu-id="16e01-116">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="16e01-116">Resource Group Name</span></span>

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

### <span data-ttu-id="16e01-117">-Slot</span><span class="sxs-lookup"><span data-stu-id="16e01-117">-Slot</span></span>
<span data-ttu-id="16e01-118">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="16e01-118">WebApp Slot Name</span></span>

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

### <span data-ttu-id="16e01-119">-Web App</span><span class="sxs-lookup"><span data-stu-id="16e01-119">-WebApp</span></span>
<span data-ttu-id="16e01-120">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="16e01-120">WebApp Object</span></span>

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

### <span data-ttu-id="16e01-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16e01-121">-DefaultProfile</span></span>
<span data-ttu-id="16e01-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="16e01-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16e01-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16e01-123">CommonParameters</span></span>
<span data-ttu-id="16e01-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16e01-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16e01-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16e01-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16e01-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="16e01-126">INPUTS</span></span>

### <span data-ttu-id="16e01-127">Sito</span><span class="sxs-lookup"><span data-stu-id="16e01-127">Site</span></span>
<span data-ttu-id="16e01-128">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="16e01-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="16e01-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="16e01-129">OUTPUTS</span></span>

## <span data-ttu-id="16e01-130">Note</span><span class="sxs-lookup"><span data-stu-id="16e01-130">NOTES</span></span>

## <span data-ttu-id="16e01-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="16e01-131">RELATED LINKS</span></span>

[<span data-ttu-id="16e01-132">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="16e01-132">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="16e01-133">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="16e01-133">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="16e01-134">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="16e01-134">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="16e01-135">Riavviare-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="16e01-135">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="16e01-136">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="16e01-136">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="16e01-137">Stop-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="16e01-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="16e01-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="16e01-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

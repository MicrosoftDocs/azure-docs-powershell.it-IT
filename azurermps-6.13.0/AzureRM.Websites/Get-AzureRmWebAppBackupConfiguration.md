---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: 81c9d87ecd93097c7e114a312b68d25d7dd681c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685548"
---
# <span data-ttu-id="acc09-101">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="acc09-101">Get-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="acc09-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="acc09-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acc09-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="acc09-103">SYNTAX</span></span>

### <span data-ttu-id="acc09-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="acc09-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acc09-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="acc09-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="acc09-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="acc09-106">DESCRIPTION</span></span>
<span data-ttu-id="acc09-107">Il cmdlet **Get-AzureRmWebAppBackupConfiguration** ottiene la configurazione di backup di una Web App Azure.</span><span class="sxs-lookup"><span data-stu-id="acc09-107">The **Get-AzureRmWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="acc09-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="acc09-108">EXAMPLES</span></span>

### <span data-ttu-id="acc09-109">1:</span><span class="sxs-lookup"><span data-stu-id="acc09-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="acc09-110">Questo comando consente di ottenere la configurazione di backup dall'app Web denominata WebAppStandard che appartiene al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="acc09-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="acc09-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="acc09-111">PARAMETERS</span></span>

### <span data-ttu-id="acc09-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acc09-112">-DefaultProfile</span></span>
<span data-ttu-id="acc09-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="acc09-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acc09-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="acc09-114">-Name</span></span>
<span data-ttu-id="acc09-115">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="acc09-115">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acc09-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acc09-116">-ResourceGroupName</span></span>
<span data-ttu-id="acc09-117">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="acc09-117">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acc09-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="acc09-118">-Slot</span></span>
<span data-ttu-id="acc09-119">Nome slot</span><span class="sxs-lookup"><span data-stu-id="acc09-119">Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acc09-120">-Web App</span><span class="sxs-lookup"><span data-stu-id="acc09-120">-WebApp</span></span>
<span data-ttu-id="acc09-121">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="acc09-121">WebApp Name</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="acc09-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acc09-122">CommonParameters</span></span>
<span data-ttu-id="acc09-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acc09-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acc09-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acc09-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acc09-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="acc09-125">INPUTS</span></span>

### <span data-ttu-id="acc09-126">System. String</span><span class="sxs-lookup"><span data-stu-id="acc09-126">System.String</span></span>

### <span data-ttu-id="acc09-127">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="acc09-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="acc09-128">Parametri: Web App (ByValue)</span><span class="sxs-lookup"><span data-stu-id="acc09-128">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="acc09-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="acc09-129">OUTPUTS</span></span>

### <span data-ttu-id="acc09-130">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="acc09-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="acc09-131">Note</span><span class="sxs-lookup"><span data-stu-id="acc09-131">NOTES</span></span>

## <span data-ttu-id="acc09-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="acc09-132">RELATED LINKS</span></span>

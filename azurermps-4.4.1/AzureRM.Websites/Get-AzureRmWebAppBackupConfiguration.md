---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: 426fc5c6cac67da7b0380b3a5e5e40cc1b533366
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686534"
---
# <span data-ttu-id="5dc4f-101">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="5dc4f-101">Get-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="5dc4f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5dc4f-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5dc4f-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5dc4f-103">SYNTAX</span></span>

### <span data-ttu-id="5dc4f-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="5dc4f-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5dc4f-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="5dc4f-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5dc4f-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5dc4f-106">DESCRIPTION</span></span>
<span data-ttu-id="5dc4f-107">Il cmdlet **Get-AzureRmWebAppBackupConfiguration** ottiene la configurazione di backup di una Web App Azure.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-107">The **Get-AzureRmWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="5dc4f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5dc4f-108">EXAMPLES</span></span>

### <span data-ttu-id="5dc4f-109">1:</span><span class="sxs-lookup"><span data-stu-id="5dc4f-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="5dc4f-110">Questo comando consente di ottenere la configurazione di backup dall'app Web denominata WebAppStandard che appartiene al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="5dc4f-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5dc4f-111">PARAMETERS</span></span>

### <span data-ttu-id="5dc4f-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="5dc4f-112">-Name</span></span>
<span data-ttu-id="5dc4f-113">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="5dc4f-113">WebApp Name</span></span>

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

### <span data-ttu-id="5dc4f-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dc4f-114">-ResourceGroupName</span></span>
<span data-ttu-id="5dc4f-115">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="5dc4f-115">Resource Group Name</span></span>

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

### <span data-ttu-id="5dc4f-116">-Slot</span><span class="sxs-lookup"><span data-stu-id="5dc4f-116">-Slot</span></span>
<span data-ttu-id="5dc4f-117">Nome slot</span><span class="sxs-lookup"><span data-stu-id="5dc4f-117">Slot Name</span></span>

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

### <span data-ttu-id="5dc4f-118">-Web App</span><span class="sxs-lookup"><span data-stu-id="5dc4f-118">-WebApp</span></span>
<span data-ttu-id="5dc4f-119">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="5dc4f-119">WebApp Name</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5dc4f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dc4f-120">-DefaultProfile</span></span>
<span data-ttu-id="5dc4f-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5dc4f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dc4f-122">CommonParameters</span></span>
<span data-ttu-id="5dc4f-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dc4f-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dc4f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dc4f-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5dc4f-125">INPUTS</span></span>

### <span data-ttu-id="5dc4f-126">Sito</span><span class="sxs-lookup"><span data-stu-id="5dc4f-126">Site</span></span>
<span data-ttu-id="5dc4f-127">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="5dc4f-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="5dc4f-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5dc4f-128">OUTPUTS</span></span>

### <span data-ttu-id="5dc4f-129">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="5dc4f-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="5dc4f-130">Note</span><span class="sxs-lookup"><span data-stu-id="5dc4f-130">NOTES</span></span>

## <span data-ttu-id="5dc4f-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5dc4f-131">RELATED LINKS</span></span>


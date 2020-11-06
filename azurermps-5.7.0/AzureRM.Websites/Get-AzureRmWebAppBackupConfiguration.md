---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: 895b020753d1f4191b87430b14e2b843a4524eaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507827"
---
# <span data-ttu-id="9f17e-101">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f17e-101">Get-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="9f17e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9f17e-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f17e-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9f17e-103">SYNTAX</span></span>

### <span data-ttu-id="9f17e-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="9f17e-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f17e-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="9f17e-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9f17e-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9f17e-106">DESCRIPTION</span></span>
<span data-ttu-id="9f17e-107">Il cmdlet **Get-AzureRmWebAppBackupConfiguration** ottiene la configurazione di backup di una Web App Azure.</span><span class="sxs-lookup"><span data-stu-id="9f17e-107">The **Get-AzureRmWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="9f17e-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9f17e-108">EXAMPLES</span></span>

### <span data-ttu-id="9f17e-109">1:</span><span class="sxs-lookup"><span data-stu-id="9f17e-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="9f17e-110">Questo comando consente di ottenere la configurazione di backup dall'app Web denominata WebAppStandard che appartiene al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="9f17e-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="9f17e-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9f17e-111">PARAMETERS</span></span>

### <span data-ttu-id="9f17e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f17e-112">-DefaultProfile</span></span>
<span data-ttu-id="9f17e-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9f17e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f17e-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="9f17e-114">-Name</span></span>
<span data-ttu-id="9f17e-115">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="9f17e-115">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f17e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f17e-116">-ResourceGroupName</span></span>
<span data-ttu-id="9f17e-117">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="9f17e-117">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f17e-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="9f17e-118">-Slot</span></span>
<span data-ttu-id="9f17e-119">Nome slot</span><span class="sxs-lookup"><span data-stu-id="9f17e-119">Slot Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f17e-120">-Web App</span><span class="sxs-lookup"><span data-stu-id="9f17e-120">-WebApp</span></span>
<span data-ttu-id="9f17e-121">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="9f17e-121">WebApp Name</span></span>

```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f17e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f17e-122">CommonParameters</span></span>
<span data-ttu-id="9f17e-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f17e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f17e-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f17e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f17e-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9f17e-125">INPUTS</span></span>

### <span data-ttu-id="9f17e-126">Sito</span><span class="sxs-lookup"><span data-stu-id="9f17e-126">Site</span></span>
<span data-ttu-id="9f17e-127">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="9f17e-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="9f17e-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9f17e-128">OUTPUTS</span></span>

### <span data-ttu-id="9f17e-129">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f17e-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="9f17e-130">Note</span><span class="sxs-lookup"><span data-stu-id="9f17e-130">NOTES</span></span>

## <span data-ttu-id="9f17e-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9f17e-131">RELATED LINKS</span></span>


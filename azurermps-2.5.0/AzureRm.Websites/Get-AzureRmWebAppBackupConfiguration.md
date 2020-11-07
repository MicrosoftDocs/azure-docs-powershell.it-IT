---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackupconfiguration
schema: 2.0.0
ms.openlocfilehash: 67bf9eb23318e4771c00760d18a5659526c5f45a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865994"
---
# <span data-ttu-id="e832c-101">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="e832c-101">Get-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="e832c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e832c-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e832c-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e832c-103">SYNTAX</span></span>

### <span data-ttu-id="e832c-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="e832c-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e832c-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="e832c-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e832c-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e832c-106">DESCRIPTION</span></span>
<span data-ttu-id="e832c-107">Il cmdlet **Get-AzureRmWebAppBackupConfiguration** ottiene la configurazione di backup di una Web App Azure.</span><span class="sxs-lookup"><span data-stu-id="e832c-107">The **Get-AzureRmWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="e832c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e832c-108">EXAMPLES</span></span>

### <span data-ttu-id="e832c-109">1:</span><span class="sxs-lookup"><span data-stu-id="e832c-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="e832c-110">Questo comando consente di ottenere la configurazione di backup dall'app Web denominata WebAppStandard che appartiene al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="e832c-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="e832c-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e832c-111">PARAMETERS</span></span>

### <span data-ttu-id="e832c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e832c-112">-DefaultProfile</span></span>
<span data-ttu-id="e832c-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e832c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e832c-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="e832c-114">-Name</span></span>
<span data-ttu-id="e832c-115">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="e832c-115">WebApp Name</span></span>

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

### <span data-ttu-id="e832c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e832c-116">-ResourceGroupName</span></span>
<span data-ttu-id="e832c-117">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="e832c-117">Resource Group Name</span></span>

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

### <span data-ttu-id="e832c-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="e832c-118">-Slot</span></span>
<span data-ttu-id="e832c-119">Nome slot</span><span class="sxs-lookup"><span data-stu-id="e832c-119">Slot Name</span></span>

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

### <span data-ttu-id="e832c-120">-Web App</span><span class="sxs-lookup"><span data-stu-id="e832c-120">-WebApp</span></span>
<span data-ttu-id="e832c-121">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="e832c-121">WebApp Name</span></span>

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

### <span data-ttu-id="e832c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e832c-122">CommonParameters</span></span>
<span data-ttu-id="e832c-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e832c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e832c-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e832c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e832c-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e832c-125">INPUTS</span></span>

### <span data-ttu-id="e832c-126">Sito</span><span class="sxs-lookup"><span data-stu-id="e832c-126">Site</span></span>
<span data-ttu-id="e832c-127">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="e832c-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="e832c-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e832c-128">OUTPUTS</span></span>

### <span data-ttu-id="e832c-129">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="e832c-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="e832c-130">Note</span><span class="sxs-lookup"><span data-stu-id="e832c-130">NOTES</span></span>

## <span data-ttu-id="e832c-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e832c-131">RELATED LINKS</span></span>


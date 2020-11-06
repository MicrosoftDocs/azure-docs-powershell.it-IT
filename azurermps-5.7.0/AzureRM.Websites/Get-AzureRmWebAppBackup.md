---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackup.md
ms.openlocfilehash: 87ecbd0c18d90a06b986ddbe4fd00e23d28b836c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519806"
---
# <span data-ttu-id="4b1be-101">Get-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="4b1be-101">Get-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="4b1be-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4b1be-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b1be-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4b1be-103">SYNTAX</span></span>

### <span data-ttu-id="4b1be-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="4b1be-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b1be-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="4b1be-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4b1be-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b1be-106">DESCRIPTION</span></span>
<span data-ttu-id="4b1be-107">Il cmdlet **Get-AzureRmWebAppBackup** ottiene il backup specificato di un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="4b1be-107">The **Get-AzureRmWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="4b1be-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4b1be-108">EXAMPLES</span></span>

### <span data-ttu-id="4b1be-109">1:</span><span class="sxs-lookup"><span data-stu-id="4b1be-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="4b1be-110">Questo comando ottiene il backup con ID "12345" dall'app Web denominata WebAppStandard che appartiene al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="4b1be-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="4b1be-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4b1be-111">PARAMETERS</span></span>

### <span data-ttu-id="4b1be-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="4b1be-112">-BackupId</span></span>
<span data-ttu-id="4b1be-113">ID backup</span><span class="sxs-lookup"><span data-stu-id="4b1be-113">Backup Id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b1be-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b1be-114">-DefaultProfile</span></span>
<span data-ttu-id="4b1be-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4b1be-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b1be-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="4b1be-116">-Name</span></span>
<span data-ttu-id="4b1be-117">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="4b1be-117">Webapp Name</span></span>

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

### <span data-ttu-id="4b1be-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b1be-118">-ResourceGroupName</span></span>
<span data-ttu-id="4b1be-119">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="4b1be-119">Resource Group Name</span></span>

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

### <span data-ttu-id="4b1be-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="4b1be-120">-Slot</span></span>
<span data-ttu-id="4b1be-121">Nome slot</span><span class="sxs-lookup"><span data-stu-id="4b1be-121">Slot Name</span></span>

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

### <span data-ttu-id="4b1be-122">-Web App</span><span class="sxs-lookup"><span data-stu-id="4b1be-122">-WebApp</span></span>
<span data-ttu-id="4b1be-123">Web App con pipe</span><span class="sxs-lookup"><span data-stu-id="4b1be-123">Piped WebApp</span></span>

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

### <span data-ttu-id="4b1be-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b1be-124">CommonParameters</span></span>
<span data-ttu-id="4b1be-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b1be-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b1be-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b1be-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b1be-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4b1be-127">INPUTS</span></span>

### <span data-ttu-id="4b1be-128">Sito</span><span class="sxs-lookup"><span data-stu-id="4b1be-128">Site</span></span>
<span data-ttu-id="4b1be-129">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="4b1be-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="4b1be-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4b1be-130">OUTPUTS</span></span>

### <span data-ttu-id="4b1be-131">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="4b1be-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="4b1be-132">Note</span><span class="sxs-lookup"><span data-stu-id="4b1be-132">NOTES</span></span>

## <span data-ttu-id="4b1be-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4b1be-133">RELATED LINKS</span></span>


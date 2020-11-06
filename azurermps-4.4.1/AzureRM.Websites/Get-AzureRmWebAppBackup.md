---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackup.md
ms.openlocfilehash: b88386077cd1a1e7b934b2a05126f00fa76bec18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519064"
---
# <span data-ttu-id="b2a63-101">Get-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="b2a63-101">Get-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="b2a63-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b2a63-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2a63-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2a63-103">SYNTAX</span></span>

### <span data-ttu-id="b2a63-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="b2a63-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2a63-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="b2a63-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2a63-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2a63-106">DESCRIPTION</span></span>
<span data-ttu-id="b2a63-107">Il cmdlet **Get-AzureRmWebAppBackup** ottiene il backup specificato di un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="b2a63-107">The **Get-AzureRmWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="b2a63-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2a63-108">EXAMPLES</span></span>

### <span data-ttu-id="b2a63-109">1:</span><span class="sxs-lookup"><span data-stu-id="b2a63-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="b2a63-110">Questo comando ottiene il backup con ID "12345" dall'app Web denominata WebAppStandard che appartiene al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="b2a63-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="b2a63-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b2a63-111">PARAMETERS</span></span>

### <span data-ttu-id="b2a63-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="b2a63-112">-BackupId</span></span>
<span data-ttu-id="b2a63-113">ID backup</span><span class="sxs-lookup"><span data-stu-id="b2a63-113">Backup Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2a63-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2a63-114">-Name</span></span>
<span data-ttu-id="b2a63-115">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="b2a63-115">Webapp Name</span></span>

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

### <span data-ttu-id="b2a63-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2a63-116">-ResourceGroupName</span></span>
<span data-ttu-id="b2a63-117">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="b2a63-117">Resource Group Name</span></span>

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

### <span data-ttu-id="b2a63-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="b2a63-118">-Slot</span></span>
<span data-ttu-id="b2a63-119">Nome slot</span><span class="sxs-lookup"><span data-stu-id="b2a63-119">Slot Name</span></span>

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

### <span data-ttu-id="b2a63-120">-Web App</span><span class="sxs-lookup"><span data-stu-id="b2a63-120">-WebApp</span></span>
<span data-ttu-id="b2a63-121">Web App con pipe</span><span class="sxs-lookup"><span data-stu-id="b2a63-121">Piped WebApp</span></span>

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

### <span data-ttu-id="b2a63-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2a63-122">-DefaultProfile</span></span>
<span data-ttu-id="b2a63-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b2a63-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2a63-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2a63-124">CommonParameters</span></span>
<span data-ttu-id="b2a63-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2a63-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2a63-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2a63-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2a63-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b2a63-127">INPUTS</span></span>

### <span data-ttu-id="b2a63-128">Sito</span><span class="sxs-lookup"><span data-stu-id="b2a63-128">Site</span></span>
<span data-ttu-id="b2a63-129">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="b2a63-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="b2a63-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2a63-130">OUTPUTS</span></span>

### <span data-ttu-id="b2a63-131">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="b2a63-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="b2a63-132">Note</span><span class="sxs-lookup"><span data-stu-id="b2a63-132">NOTES</span></span>

## <span data-ttu-id="b2a63-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2a63-133">RELATED LINKS</span></span>


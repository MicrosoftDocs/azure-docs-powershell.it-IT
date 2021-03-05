---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
ms.openlocfilehash: 512162485b38d6cf02ad8519131eb4252605c4a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995832"
---
# <span data-ttu-id="5a372-101">Get-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="5a372-101">Get-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="5a372-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a372-102">SYNOPSIS</span></span>
<span data-ttu-id="5a372-103">Ottiene un profilo di pubblicazione di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="5a372-103">Gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="5a372-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5a372-104">SYNTAX</span></span>

### <span data-ttu-id="5a372-105">S1</span><span class="sxs-lookup"><span data-stu-id="5a372-105">S1</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a372-106">S2</span><span class="sxs-lookup"><span data-stu-id="5a372-106">S2</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a372-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5a372-107">DESCRIPTION</span></span>
<span data-ttu-id="5a372-108">Il **cmdlet Get-AzWebAppPublishingProfile** ottiene un profilo di pubblicazione di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="5a372-108">The **Get-AzWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="5a372-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5a372-109">EXAMPLES</span></span>

### <span data-ttu-id="5a372-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5a372-110">Example 1</span></span>
```powershell
PS C:\> Get-AzWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile.publishsettings"
```

<span data-ttu-id="5a372-111">Questo comando recupera il profilo di pubblicazione in formato Ftp per l'app Web ContosoWebApp associata al gruppo di risorse Default-Web-WestUS e lo archivia nel file di output specificato.</span><span class="sxs-lookup"><span data-stu-id="5a372-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="5a372-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a372-112">PARAMETERS</span></span>

### <span data-ttu-id="5a372-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a372-113">-DefaultProfile</span></span>
<span data-ttu-id="5a372-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5a372-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a372-115">-Format</span><span class="sxs-lookup"><span data-stu-id="5a372-115">-Format</span></span>
<span data-ttu-id="5a372-116">Formato</span><span class="sxs-lookup"><span data-stu-id="5a372-116">Format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a372-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="5a372-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="5a372-118">Includere gli endpoint di ripristino di emergenza, se vero</span><span class="sxs-lookup"><span data-stu-id="5a372-118">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a372-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5a372-119">-Name</span></span>
<span data-ttu-id="5a372-120">Nome WebApp</span><span class="sxs-lookup"><span data-stu-id="5a372-120">WebApp Name</span></span>

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

### <span data-ttu-id="5a372-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="5a372-121">-OutputFile</span></span>
<span data-ttu-id="5a372-122">Output File</span><span class="sxs-lookup"><span data-stu-id="5a372-122">Output File</span></span>

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

### <span data-ttu-id="5a372-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a372-123">-ResourceGroupName</span></span>
<span data-ttu-id="5a372-124">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="5a372-124">Resource Group Name</span></span>

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

### <span data-ttu-id="5a372-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="5a372-125">-WebApp</span></span>
<span data-ttu-id="5a372-126">Oggetto WebApp</span><span class="sxs-lookup"><span data-stu-id="5a372-126">WebApp Object</span></span>

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

### <span data-ttu-id="5a372-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a372-127">CommonParameters</span></span>
<span data-ttu-id="5a372-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a372-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a372-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a372-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a372-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="5a372-130">INPUTS</span></span>

### <span data-ttu-id="5a372-131">System.String</span><span class="sxs-lookup"><span data-stu-id="5a372-131">System.String</span></span>

### <span data-ttu-id="5a372-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="5a372-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="5a372-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5a372-133">OUTPUTS</span></span>

### <span data-ttu-id="5a372-134">System.String</span><span class="sxs-lookup"><span data-stu-id="5a372-134">System.String</span></span>

## <span data-ttu-id="5a372-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="5a372-135">NOTES</span></span>

## <span data-ttu-id="5a372-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5a372-136">RELATED LINKS</span></span>

[<span data-ttu-id="5a372-137">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5a372-137">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="5a372-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5a372-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)



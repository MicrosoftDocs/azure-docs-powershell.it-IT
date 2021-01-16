---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 8ef8639c2ff79a326a8d0ffcdf1f1dca24dbccf9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326897"
---
# <span data-ttu-id="4489f-101">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="4489f-101">Get-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="4489f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4489f-102">SYNOPSIS</span></span>

## <span data-ttu-id="4489f-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4489f-103">SYNTAX</span></span>

### <span data-ttu-id="4489f-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="4489f-104">FromResourceName</span></span>
```
Get-AzWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4489f-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="4489f-105">FromWebApp</span></span>
```
Get-AzWebAppBackupConfiguration [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4489f-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4489f-106">DESCRIPTION</span></span>
<span data-ttu-id="4489f-107">Il cmdlet **Get-AzWebAppBackupConfiguration** ottiene la configurazione di backup di una Web App Azure.</span><span class="sxs-lookup"><span data-stu-id="4489f-107">The **Get-AzWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="4489f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4489f-108">EXAMPLES</span></span>

### <span data-ttu-id="4489f-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4489f-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="4489f-110">Questo comando consente di ottenere la configurazione di backup dall'app Web denominata WebAppStandard che appartiene al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="4489f-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="4489f-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4489f-111">PARAMETERS</span></span>

### <span data-ttu-id="4489f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4489f-112">-DefaultProfile</span></span>
<span data-ttu-id="4489f-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4489f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4489f-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="4489f-114">-Name</span></span>
<span data-ttu-id="4489f-115">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="4489f-115">WebApp Name</span></span>

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

### <span data-ttu-id="4489f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4489f-116">-ResourceGroupName</span></span>
<span data-ttu-id="4489f-117">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="4489f-117">Resource Group Name</span></span>

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

### <span data-ttu-id="4489f-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="4489f-118">-Slot</span></span>
<span data-ttu-id="4489f-119">Nome slot</span><span class="sxs-lookup"><span data-stu-id="4489f-119">Slot Name</span></span>

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

### <span data-ttu-id="4489f-120">-Web App</span><span class="sxs-lookup"><span data-stu-id="4489f-120">-WebApp</span></span>
<span data-ttu-id="4489f-121">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="4489f-121">WebApp Name</span></span>

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

### <span data-ttu-id="4489f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4489f-122">CommonParameters</span></span>
<span data-ttu-id="4489f-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4489f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4489f-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4489f-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4489f-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4489f-125">INPUTS</span></span>

### <span data-ttu-id="4489f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="4489f-126">System.String</span></span>

### <span data-ttu-id="4489f-127">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="4489f-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="4489f-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4489f-128">OUTPUTS</span></span>

### <span data-ttu-id="4489f-129">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="4489f-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="4489f-130">Note</span><span class="sxs-lookup"><span data-stu-id="4489f-130">NOTES</span></span>

## <span data-ttu-id="4489f-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4489f-131">RELATED LINKS</span></span>

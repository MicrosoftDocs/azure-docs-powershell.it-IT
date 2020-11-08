---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: 350f7d5b44f5a1c84f97511a4febb7d967ee2de4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191392"
---
# <span data-ttu-id="a6b1b-101">Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="a6b1b-101">Get-AzWebAppSnapshot</span></span>

## <span data-ttu-id="a6b1b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a6b1b-102">SYNOPSIS</span></span>
<span data-ttu-id="a6b1b-103">Ottiene gli snapshot disponibili per un'app Web.</span><span class="sxs-lookup"><span data-stu-id="a6b1b-103">Gets the snapshots available for a web app.</span></span>

## <span data-ttu-id="a6b1b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6b1b-104">SYNTAX</span></span>

### <span data-ttu-id="a6b1b-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="a6b1b-105">FromResourceName</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6b1b-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="a6b1b-106">FromWebApp</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a6b1b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6b1b-107">DESCRIPTION</span></span>
<span data-ttu-id="a6b1b-108">Il cmdlet **Get-AzWebAppSnapshot** restituisce tutti gli snapshot per un'app Web.</span><span class="sxs-lookup"><span data-stu-id="a6b1b-108">The **Get-AzWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="a6b1b-109">Gli snapshot sono backup automatici dei file e delle impostazioni di un'app Web.</span><span class="sxs-lookup"><span data-stu-id="a6b1b-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="a6b1b-110">Uno snapshot può essere ripristinato con il cmdlet **Restore-AzWebAppSnapshot** .</span><span class="sxs-lookup"><span data-stu-id="a6b1b-110">A snapshot can be restored with the **Restore-AzWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="a6b1b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6b1b-111">EXAMPLES</span></span>

### <span data-ttu-id="a6b1b-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a6b1b-112">Example 1</span></span>
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="a6b1b-113">Ottenere gli snapshot per un'app Web denominata "ContosoApp" con uno slot denominato "Staging" nel gruppo di risorse "predefinito-Web-Westus"</span><span class="sxs-lookup"><span data-stu-id="a6b1b-113">Get the snapshots for a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="a6b1b-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a6b1b-114">PARAMETERS</span></span>

### <span data-ttu-id="a6b1b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6b1b-115">-DefaultProfile</span></span>
<span data-ttu-id="a6b1b-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a6b1b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6b1b-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="a6b1b-117">-Name</span></span>
<span data-ttu-id="a6b1b-118">Nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="a6b1b-118">The name of the web app.</span></span>

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

### <span data-ttu-id="a6b1b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6b1b-119">-ResourceGroupName</span></span>
<span data-ttu-id="a6b1b-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a6b1b-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="a6b1b-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="a6b1b-121">-Slot</span></span>
<span data-ttu-id="a6b1b-122">Il nome dello slot Web App.</span><span class="sxs-lookup"><span data-stu-id="a6b1b-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="a6b1b-123">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="a6b1b-123">-UseDisasterRecovery</span></span>
<span data-ttu-id="a6b1b-124">Leggere le istantanee da un'unità di scala secondaria.</span><span class="sxs-lookup"><span data-stu-id="a6b1b-124">Read the snapshots from a secondary scale unit.</span></span>

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

### <span data-ttu-id="a6b1b-125">-Web App</span><span class="sxs-lookup"><span data-stu-id="a6b1b-125">-WebApp</span></span>
<span data-ttu-id="a6b1b-126">Oggetto app Web</span><span class="sxs-lookup"><span data-stu-id="a6b1b-126">The web app object</span></span>

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

### <span data-ttu-id="a6b1b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6b1b-127">CommonParameters</span></span>
<span data-ttu-id="a6b1b-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6b1b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6b1b-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6b1b-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6b1b-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a6b1b-130">INPUTS</span></span>

### <span data-ttu-id="a6b1b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a6b1b-131">System.String</span></span>

### <span data-ttu-id="a6b1b-132">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="a6b1b-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a6b1b-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6b1b-133">OUTPUTS</span></span>

### <span data-ttu-id="a6b1b-134">Microsoft. Azure. Commands. webapps. Cmdlets. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="a6b1b-134">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="a6b1b-135">Note</span><span class="sxs-lookup"><span data-stu-id="a6b1b-135">NOTES</span></span>

## <span data-ttu-id="a6b1b-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6b1b-136">RELATED LINKS</span></span>
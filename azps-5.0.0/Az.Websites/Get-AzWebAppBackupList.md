---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
ms.openlocfilehash: 6ea805f1e3a3711c2efe6faefd73edf06c4b51fd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301662"
---
# <span data-ttu-id="0bb8f-101">Get-AzWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="0bb8f-101">Get-AzWebAppBackupList</span></span>

## <span data-ttu-id="0bb8f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0bb8f-102">SYNOPSIS</span></span>

## <span data-ttu-id="0bb8f-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0bb8f-103">SYNTAX</span></span>

### <span data-ttu-id="0bb8f-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="0bb8f-104">FromResourceName</span></span>
```
Get-AzWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bb8f-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="0bb8f-105">FromWebApp</span></span>
```
Get-AzWebAppBackupList [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bb8f-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0bb8f-106">DESCRIPTION</span></span>
<span data-ttu-id="0bb8f-107">Il cmdlet **Get-AzWebAppBackupList** ottiene un elenco di backup per un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="0bb8f-107">The **Get-AzWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="0bb8f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0bb8f-108">EXAMPLES</span></span>

### <span data-ttu-id="0bb8f-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0bb8f-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="0bb8f-110">Questo comando restituisce un elenco di backup relativo a Web App WebAppStandard associato al gruppo di risorse ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0bb8f-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="0bb8f-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0bb8f-111">PARAMETERS</span></span>

### <span data-ttu-id="0bb8f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bb8f-112">-DefaultProfile</span></span>
<span data-ttu-id="0bb8f-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0bb8f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bb8f-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="0bb8f-114">-Name</span></span>
<span data-ttu-id="0bb8f-115">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="0bb8f-115">WebApp Name</span></span>

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

### <span data-ttu-id="0bb8f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bb8f-116">-ResourceGroupName</span></span>
<span data-ttu-id="0bb8f-117">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="0bb8f-117">Resource Group Name</span></span>

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

### <span data-ttu-id="0bb8f-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="0bb8f-118">-Slot</span></span>
<span data-ttu-id="0bb8f-119">Nome slot</span><span class="sxs-lookup"><span data-stu-id="0bb8f-119">Slot name</span></span>

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

### <span data-ttu-id="0bb8f-120">-Web App</span><span class="sxs-lookup"><span data-stu-id="0bb8f-120">-WebApp</span></span>
<span data-ttu-id="0bb8f-121">Web App con pipe</span><span class="sxs-lookup"><span data-stu-id="0bb8f-121">Piped WebApp</span></span>

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

### <span data-ttu-id="0bb8f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bb8f-122">CommonParameters</span></span>
<span data-ttu-id="0bb8f-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bb8f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bb8f-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bb8f-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bb8f-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0bb8f-125">INPUTS</span></span>

### <span data-ttu-id="0bb8f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="0bb8f-126">System.String</span></span>

### <span data-ttu-id="0bb8f-127">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="0bb8f-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0bb8f-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0bb8f-128">OUTPUTS</span></span>

### <span data-ttu-id="0bb8f-129">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="0bb8f-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="0bb8f-130">Note</span><span class="sxs-lookup"><span data-stu-id="0bb8f-130">NOTES</span></span>

## <span data-ttu-id="0bb8f-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0bb8f-131">RELATED LINKS</span></span>

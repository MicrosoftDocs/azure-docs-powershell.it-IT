---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
ms.openlocfilehash: b60b43b2c0a28be969ad633c80338f42b2c98db6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180838"
---
# <span data-ttu-id="7240a-101">Get-AzDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="7240a-101">Get-AzDataShareSynchronization</span></span>

## <span data-ttu-id="7240a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7240a-102">SYNOPSIS</span></span>
<span data-ttu-id="7240a-103">Recupera informazioni sull'impostazione di sincronizzazione per una condivisione.</span><span class="sxs-lookup"><span data-stu-id="7240a-103">Gets information about synchronization setting for a share.</span></span>

## <span data-ttu-id="7240a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7240a-104">SYNTAX</span></span>

### <span data-ttu-id="7240a-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7240a-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronization -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7240a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7240a-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7240a-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7240a-107">DESCRIPTION</span></span>
<span data-ttu-id="7240a-108">Il cmdlet **Get-AzDataShareSynchronization** fornisce informazioni su tutte le impostazioni di sincronizzazione presenti in una condivisione con un account di condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="7240a-108">The **Get-AzDataShareSynchronization** cmdlet provides information about all the synchronization setting present in a share under a data share account.</span></span>

## <span data-ttu-id="7240a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7240a-109">EXAMPLES</span></span>

### <span data-ttu-id="7240a-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7240a-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare"

Company           : ADS Test
DurationMs        : 107013
EndTime           : 7/8/2019 11:53:18 PM
Message           :
StartTime         : 7/8/2019 11:51:34 PM
Status            : Succeeded
SynchronizationId : e6dc7080-6589-4628-8b50-8fc31b460089
```

<span data-ttu-id="7240a-111">Questo comando fornisce informazioni su tutte le impostazioni di sincronizzazione presenti in Share AdsShare nell'account di condivisione dati WikiAds.</span><span class="sxs-lookup"><span data-stu-id="7240a-111">This commands provides information about all synchronization settings present in share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="7240a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7240a-112">PARAMETERS</span></span>

### <span data-ttu-id="7240a-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7240a-113">-AccountName</span></span>
<span data-ttu-id="7240a-114">Nome account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="7240a-114">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7240a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7240a-115">-DefaultProfile</span></span>
<span data-ttu-id="7240a-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7240a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7240a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7240a-117">-ResourceGroupName</span></span>
<span data-ttu-id="7240a-118">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="7240a-118">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7240a-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7240a-119">-ResourceId</span></span>
<span data-ttu-id="7240a-120">ID risorsa condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="7240a-120">Azure data share resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7240a-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="7240a-121">-ShareName</span></span>
<span data-ttu-id="7240a-122">Nome condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="7240a-122">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7240a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7240a-123">CommonParameters</span></span>
<span data-ttu-id="7240a-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7240a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7240a-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7240a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7240a-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="7240a-126">INPUTS</span></span>

### <span data-ttu-id="7240a-127">System.String</span><span class="sxs-lookup"><span data-stu-id="7240a-127">System.String</span></span>

## <span data-ttu-id="7240a-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7240a-128">OUTPUTS</span></span>

### <span data-ttu-id="7240a-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="7240a-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span></span>

## <span data-ttu-id="7240a-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="7240a-130">NOTES</span></span>

## <span data-ttu-id="7240a-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7240a-131">RELATED LINKS</span></span>

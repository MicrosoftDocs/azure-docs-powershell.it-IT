---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 183164c3f2a18e68b9eab3f505f382a161abf415
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180830"
---
# <span data-ttu-id="1df55-101">Get-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="1df55-101">Get-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="1df55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1df55-102">SYNOPSIS</span></span>
<span data-ttu-id="1df55-103">Ottiene informazioni sull'impostazione di sincronizzazione in una condivisione.</span><span class="sxs-lookup"><span data-stu-id="1df55-103">Gets information about synchronization setting on a share.</span></span>

## <span data-ttu-id="1df55-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1df55-104">SYNTAX</span></span>

### <span data-ttu-id="1df55-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1df55-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1df55-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1df55-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1df55-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1df55-107">DESCRIPTION</span></span>
<span data-ttu-id="1df55-108">Il cmdlet **Get-AzDataShareSynchronizationSetting** fornisce informazioni sulla sincronizzazione abilitata in una condivisione.</span><span class="sxs-lookup"><span data-stu-id="1df55-108">The **Get-AzDataShareSynchronizationSetting** cmdlet provides information about synchronization enabled on a share.</span></span> 

## <span data-ttu-id="1df55-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1df55-109">EXAMPLES</span></span>

### <span data-ttu-id="1df55-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1df55-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ShareSynchronization"

RecurrenceInterval  : Day
SynchronizationTime : 7/9/2019 9:00:00 AM
ProvisioningState   : Succeeded
CreatedAt           : 7/10/2019 12:01:08 AM
CreatedBy           : ADS Test
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.
                      DataShare/accounts/WikiAds/shares/AdShare/synchronizationSettings/ShareSynchronization
Name                : ShareSynchronization
Type                : Microsoft.DataShare/SynchronizationSettings
```

<span data-ttu-id="1df55-111">Questo comando fornisce informazioni sulla sincronizzazione di ShareSynchronization abilitata in Share AdsShare nell'account di condivisione dati WikiAds.</span><span class="sxs-lookup"><span data-stu-id="1df55-111">This command provides information about synchronization ShareSynchronization enabled on share AdsShare under data share account WikiAds.</span></span>

## <span data-ttu-id="1df55-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1df55-112">PARAMETERS</span></span>

### <span data-ttu-id="1df55-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1df55-113">-AccountName</span></span>
<span data-ttu-id="1df55-114">Nome account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="1df55-114">Azure data share account name</span></span>

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

### <span data-ttu-id="1df55-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1df55-115">-DefaultProfile</span></span>
<span data-ttu-id="1df55-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1df55-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1df55-117">-Name</span><span class="sxs-lookup"><span data-stu-id="1df55-117">-Name</span></span>
<span data-ttu-id="1df55-118">Nome per l'impostazione di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="1df55-118">Name for Synchronization Setting</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1df55-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1df55-119">-ResourceGroupName</span></span>
<span data-ttu-id="1df55-120">Nome del gruppo di risorse dell'account azure data share</span><span class="sxs-lookup"><span data-stu-id="1df55-120">Resource group name of azure data share account</span></span>

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

### <span data-ttu-id="1df55-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1df55-121">-ResourceId</span></span>
<span data-ttu-id="1df55-122">ID risorsa dell'impostazione di sincronizzazione della condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="1df55-122">The resource id of the azure data share synchronization setting</span></span>

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

### <span data-ttu-id="1df55-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="1df55-123">-ShareName</span></span>
<span data-ttu-id="1df55-124">Nome condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="1df55-124">Azure data share name</span></span>

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

### <span data-ttu-id="1df55-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1df55-125">CommonParameters</span></span>
<span data-ttu-id="1df55-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1df55-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1df55-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1df55-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1df55-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="1df55-128">INPUTS</span></span>

### <span data-ttu-id="1df55-129">System.String</span><span class="sxs-lookup"><span data-stu-id="1df55-129">System.String</span></span>

## <span data-ttu-id="1df55-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1df55-130">OUTPUTS</span></span>

### <span data-ttu-id="1df55-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="1df55-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="1df55-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="1df55-132">NOTES</span></span>

## <span data-ttu-id="1df55-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1df55-133">RELATED LINKS</span></span>

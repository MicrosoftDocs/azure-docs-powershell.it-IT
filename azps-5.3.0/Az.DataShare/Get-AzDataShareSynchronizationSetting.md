---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 183164c3f2a18e68b9eab3f505f382a161abf415
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377355"
---
# <span data-ttu-id="75507-101">Get-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="75507-101">Get-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="75507-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="75507-102">SYNOPSIS</span></span>
<span data-ttu-id="75507-103">Ottiene informazioni sull'impostazione della sincronizzazione in una condivisione.</span><span class="sxs-lookup"><span data-stu-id="75507-103">Gets information about synchronization setting on a share.</span></span>

## <span data-ttu-id="75507-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="75507-104">SYNTAX</span></span>

### <span data-ttu-id="75507-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="75507-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75507-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75507-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="75507-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75507-107">DESCRIPTION</span></span>
<span data-ttu-id="75507-108">Il cmdlet **Get-AzDataShareSynchronizationSetting** fornisce informazioni sulla sincronizzazione abilitata per una condivisione.</span><span class="sxs-lookup"><span data-stu-id="75507-108">The **Get-AzDataShareSynchronizationSetting** cmdlet provides information about synchronization enabled on a share.</span></span> 

## <span data-ttu-id="75507-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="75507-109">EXAMPLES</span></span>

### <span data-ttu-id="75507-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="75507-110">Example 1</span></span>
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

<span data-ttu-id="75507-111">Questo comando fornisce informazioni sulla sincronizzazione ShareSynchronization abilitata in Condividi AdsShare in WikiAds account di condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="75507-111">This command provides information about synchronization ShareSynchronization enabled on share AdsShare under data share account WikiAds.</span></span>

## <span data-ttu-id="75507-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="75507-112">PARAMETERS</span></span>

### <span data-ttu-id="75507-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="75507-113">-AccountName</span></span>
<span data-ttu-id="75507-114">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="75507-114">Azure data share account name</span></span>

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

### <span data-ttu-id="75507-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75507-115">-DefaultProfile</span></span>
<span data-ttu-id="75507-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="75507-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75507-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="75507-117">-Name</span></span>
<span data-ttu-id="75507-118">Nome per l'impostazione della sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="75507-118">Name for Synchronization Setting</span></span>

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

### <span data-ttu-id="75507-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75507-119">-ResourceGroupName</span></span>
<span data-ttu-id="75507-120">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="75507-120">Resource group name of azure data share account</span></span>

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

### <span data-ttu-id="75507-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75507-121">-ResourceId</span></span>
<span data-ttu-id="75507-122">ID risorsa dell'impostazione di sincronizzazione della condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="75507-122">The resource id of the azure data share synchronization setting</span></span>

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

### <span data-ttu-id="75507-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="75507-123">-ShareName</span></span>
<span data-ttu-id="75507-124">Nome condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="75507-124">Azure data share name</span></span>

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

### <span data-ttu-id="75507-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75507-125">CommonParameters</span></span>
<span data-ttu-id="75507-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75507-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75507-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75507-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75507-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="75507-128">INPUTS</span></span>

### <span data-ttu-id="75507-129">System. String</span><span class="sxs-lookup"><span data-stu-id="75507-129">System.String</span></span>

## <span data-ttu-id="75507-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="75507-130">OUTPUTS</span></span>

### <span data-ttu-id="75507-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="75507-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="75507-132">Note</span><span class="sxs-lookup"><span data-stu-id="75507-132">NOTES</span></span>

## <span data-ttu-id="75507-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="75507-133">RELATED LINKS</span></span>

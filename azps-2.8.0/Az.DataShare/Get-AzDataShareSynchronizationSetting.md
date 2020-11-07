---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 9dca6272991c67375f2764725901018c331e0ca9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674679"
---
# <span data-ttu-id="bfd29-101">Get-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="bfd29-101">Get-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="bfd29-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bfd29-102">SYNOPSIS</span></span>
<span data-ttu-id="bfd29-103">Ottiene informazioni sull'impostazione della sincronizzazione in una condivisione.</span><span class="sxs-lookup"><span data-stu-id="bfd29-103">Gets information about synchronization setting on a share.</span></span>

## <span data-ttu-id="bfd29-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bfd29-104">SYNTAX</span></span>

### <span data-ttu-id="bfd29-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bfd29-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfd29-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfd29-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bfd29-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bfd29-107">DESCRIPTION</span></span>
<span data-ttu-id="bfd29-108">Il cmdlet **Get-AzDataShareSynchronizationSetting** fornisce informazioni sulla sincronizzazione abilitata per una condivisione.</span><span class="sxs-lookup"><span data-stu-id="bfd29-108">The **Get-AzDataShareSynchronizationSetting** cmdlet provides information about synchronization enabled on a share.</span></span> 

## <span data-ttu-id="bfd29-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bfd29-109">EXAMPLES</span></span>

### <span data-ttu-id="bfd29-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bfd29-110">Example 1</span></span>
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

<span data-ttu-id="bfd29-111">Questo comando fornisce informazioni sulla sincronizzazione ShareSynchronization abilitata in Condividi AdsShare in WikiAds account di condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="bfd29-111">This command provides information about synchronization ShareSynchronization enabled on share AdsShare under data share account WikiAds.</span></span>

## <span data-ttu-id="bfd29-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bfd29-112">PARAMETERS</span></span>

### <span data-ttu-id="bfd29-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bfd29-113">-AccountName</span></span>
<span data-ttu-id="bfd29-114">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="bfd29-114">Azure data share account name</span></span>

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

### <span data-ttu-id="bfd29-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfd29-115">-DefaultProfile</span></span>
<span data-ttu-id="bfd29-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bfd29-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfd29-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="bfd29-117">-Name</span></span>
<span data-ttu-id="bfd29-118">Nome per l'impostazione della sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="bfd29-118">Name for Synchronization Setting</span></span>

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

### <span data-ttu-id="bfd29-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfd29-119">-ResourceGroupName</span></span>
<span data-ttu-id="bfd29-120">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="bfd29-120">Resource group name of azure data share account</span></span>

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

### <span data-ttu-id="bfd29-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bfd29-121">-ResourceId</span></span>
<span data-ttu-id="bfd29-122">ID risorsa dell'impostazione di sincronizzazione della condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="bfd29-122">The resource id of the azure data share synchronization setting</span></span>

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

### <span data-ttu-id="bfd29-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="bfd29-123">-ShareName</span></span>
<span data-ttu-id="bfd29-124">Nome condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="bfd29-124">Azure data share name</span></span>

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

### <span data-ttu-id="bfd29-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfd29-125">CommonParameters</span></span>
<span data-ttu-id="bfd29-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfd29-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfd29-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfd29-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfd29-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bfd29-128">INPUTS</span></span>

### <span data-ttu-id="bfd29-129">System. String</span><span class="sxs-lookup"><span data-stu-id="bfd29-129">System.String</span></span>

## <span data-ttu-id="bfd29-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bfd29-130">OUTPUTS</span></span>

### <span data-ttu-id="bfd29-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="bfd29-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="bfd29-132">Note</span><span class="sxs-lookup"><span data-stu-id="bfd29-132">NOTES</span></span>

## <span data-ttu-id="bfd29-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bfd29-133">RELATED LINKS</span></span>

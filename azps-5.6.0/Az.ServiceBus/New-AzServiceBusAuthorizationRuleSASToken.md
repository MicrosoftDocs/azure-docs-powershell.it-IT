---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/new-azservicebusauthorizationrulesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRuleSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRuleSASToken.md
ms.openlocfilehash: 313022f4d622058594398b72dfd917e18cfaec77
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978125"
---
# <span data-ttu-id="305b0-101">New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="305b0-101">New-AzServiceBusAuthorizationRuleSASToken</span></span>

## <span data-ttu-id="305b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="305b0-102">SYNOPSIS</span></span>
<span data-ttu-id="305b0-103">Genera una regola di autorizzazione sas per azure servicebus dello spazio dei nomi, della coda/argomento.</span><span class="sxs-lookup"><span data-stu-id="305b0-103">Generates a SAS tolen for Azure servicebus authorization rule of namespace/queue/topic.</span></span> 

## <span data-ttu-id="305b0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="305b0-104">SYNTAX</span></span>

```
New-AzServiceBusAuthorizationRuleSASToken [-AuthorizationRuleId] <String> [-KeyType] <String>
 [-ExpiryTime] <DateTime> [-StartTime <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="305b0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="305b0-105">DESCRIPTION</span></span>
<span data-ttu-id="305b0-106">Il cmdlet New-AzServiceBusAuthorizationRuleSASToken genera un token di firma di accesso condiviso per un nome Azure Eventhub Namesapce o Azure Eventhub</span><span class="sxs-lookup"><span data-stu-id="305b0-106">The New-AzServiceBusAuthorizationRuleSASToken cmdlet generates a Shared Access Signature (SAS) token for an Azure Eventhub Namesapce or Azure Eventhub</span></span>

## <span data-ttu-id="305b0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="305b0-107">EXAMPLES</span></span>

### <span data-ttu-id="305b0-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="305b0-108">Example 1</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzServiceBusAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime -StartTime $StartTime
```

<span data-ttu-id="305b0-109">Genera token di firma di accesso condiviso per la regola di autorizzazione specificata per Spazio dei nomi con data di inizio e scadenza.</span><span class="sxs-lookup"><span data-stu-id="305b0-109">Generate SAS token for the given authorixation rule for Namespace with start and expiry time..</span></span>

### <span data-ttu-id="305b0-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="305b0-110">Example 2</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzServiceBusAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime
```

<span data-ttu-id="305b0-111">Generare il token di firma di accesso condiviso per la regola di autorizzazione specificata per Spazio dei nomi con scadenza.</span><span class="sxs-lookup"><span data-stu-id="305b0-111">Generate SAS token for the given authorixation rule for Namespace with expiry time.</span></span>

## <span data-ttu-id="305b0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="305b0-112">PARAMETERS</span></span>

### <span data-ttu-id="305b0-113">-AuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="305b0-113">-AuthorizationRuleId</span></span>
<span data-ttu-id="305b0-114">ARM ResourceId della regola di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="305b0-114">ARM ResourceId of the Authoraization Rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="305b0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="305b0-115">-DefaultProfile</span></span>
<span data-ttu-id="305b0-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="305b0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="305b0-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="305b0-117">-ExpiryTime</span></span>
<span data-ttu-id="305b0-118">Ora scadenza</span><span class="sxs-lookup"><span data-stu-id="305b0-118">Expiry Time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="305b0-119">-KeyType</span><span class="sxs-lookup"><span data-stu-id="305b0-119">-KeyType</span></span>
<span data-ttu-id="305b0-120">Tipo di tasto</span><span class="sxs-lookup"><span data-stu-id="305b0-120">Key Type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="305b0-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="305b0-121">-StartTime</span></span>
<span data-ttu-id="305b0-122">Ora inizio</span><span class="sxs-lookup"><span data-stu-id="305b0-122">Start Time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="305b0-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="305b0-123">-Confirm</span></span>
<span data-ttu-id="305b0-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="305b0-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="305b0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="305b0-125">-WhatIf</span></span>
<span data-ttu-id="305b0-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="305b0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="305b0-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="305b0-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="305b0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="305b0-128">CommonParameters</span></span>
<span data-ttu-id="305b0-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="305b0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="305b0-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="305b0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="305b0-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="305b0-131">INPUTS</span></span>

### <span data-ttu-id="305b0-132">System.String</span><span class="sxs-lookup"><span data-stu-id="305b0-132">System.String</span></span>

### <span data-ttu-id="305b0-133">System.Nullable'1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="305b0-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="305b0-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="305b0-134">OUTPUTS</span></span>

### <span data-ttu-id="305b0-135">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessSignatureAttributes</span><span class="sxs-lookup"><span data-stu-id="305b0-135">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessSignatureAttributes</span></span>

## <span data-ttu-id="305b0-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="305b0-136">NOTES</span></span>

## <span data-ttu-id="305b0-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="305b0-137">RELATED LINKS</span></span>
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubauthorizationrulesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRuleSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRuleSASToken.md
ms.openlocfilehash: 24348c44ef9b529507c50a689f181739d1474e22
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332299"
---
# <span data-ttu-id="b69ba-101">New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="b69ba-101">New-AzEventHubAuthorizationRuleSASToken</span></span>

## <span data-ttu-id="b69ba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b69ba-102">SYNOPSIS</span></span>
<span data-ttu-id="b69ba-103">Genera un token SAS per la regola di autorizzazione di Azure eventhub dello spazio dei nomi/eventhub.</span><span class="sxs-lookup"><span data-stu-id="b69ba-103">Generates a SAS token for Azure eventhub authorization rule of namespace/eventhub.</span></span> 

## <span data-ttu-id="b69ba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b69ba-104">SYNTAX</span></span>

```
New-AzEventHubAuthorizationRuleSASToken [-AuthorizationRuleId] <String> [-KeyType] <String>
 [-ExpiryTime] <DateTime> [-StartTime <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b69ba-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b69ba-105">DESCRIPTION</span></span>
<span data-ttu-id="b69ba-106">Il cmdlet New-AzEventHubAuthorizationRuleSASToken genera un token SAS (Shared Access Signature) per un file Azure Eventhub o un Eventhub di Azure</span><span class="sxs-lookup"><span data-stu-id="b69ba-106">The New-AzEventHubAuthorizationRuleSASToken cmdlet generates a Shared Access Signature (SAS) token for an Azure Eventhub Namesapce or Azure Eventhub</span></span>

## <span data-ttu-id="b69ba-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b69ba-107">EXAMPLES</span></span>

### <span data-ttu-id="b69ba-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b69ba-108">Example 1</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzEventHubAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime -StartTime $StartTime
```

<span data-ttu-id="b69ba-109">Genera il token SAS per la regola authorixation specificata per lo spazio dei nomi con l'ora di inizio e di scadenza.</span><span class="sxs-lookup"><span data-stu-id="b69ba-109">Generate SAS token for the given authorixation rule for Namespace with start and expiry time..</span></span>

### <span data-ttu-id="b69ba-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b69ba-110">Example 2</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzEventHubAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime
```

<span data-ttu-id="b69ba-111">Genera il token SAS per la regola authorixation specificata per lo spazio dei nomi con tempo di scadenza.</span><span class="sxs-lookup"><span data-stu-id="b69ba-111">Generate SAS token for the given authorixation rule for Namespace with expiry time.</span></span>

## <span data-ttu-id="b69ba-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b69ba-112">PARAMETERS</span></span>

### <span data-ttu-id="b69ba-113">-AuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="b69ba-113">-AuthorizationRuleId</span></span>
<span data-ttu-id="b69ba-114">ARM ResourceId della regola Authoraization</span><span class="sxs-lookup"><span data-stu-id="b69ba-114">ARM ResourceId of the Authoraization Rule</span></span>

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

### <span data-ttu-id="b69ba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b69ba-115">-DefaultProfile</span></span>
<span data-ttu-id="b69ba-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b69ba-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b69ba-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b69ba-117">-ExpiryTime</span></span>
<span data-ttu-id="b69ba-118">Ora di scadenza</span><span class="sxs-lookup"><span data-stu-id="b69ba-118">Expiry Time</span></span>

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

### <span data-ttu-id="b69ba-119">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="b69ba-119">-KeyType</span></span>
<span data-ttu-id="b69ba-120">Tipo di chiave</span><span class="sxs-lookup"><span data-stu-id="b69ba-120">Key Type</span></span>

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

### <span data-ttu-id="b69ba-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b69ba-121">-StartTime</span></span>
<span data-ttu-id="b69ba-122">Ora di inizio</span><span class="sxs-lookup"><span data-stu-id="b69ba-122">Start Time</span></span>

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

### <span data-ttu-id="b69ba-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b69ba-123">-Confirm</span></span>
<span data-ttu-id="b69ba-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b69ba-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b69ba-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b69ba-125">-WhatIf</span></span>
<span data-ttu-id="b69ba-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b69ba-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b69ba-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b69ba-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b69ba-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b69ba-128">CommonParameters</span></span>
<span data-ttu-id="b69ba-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b69ba-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b69ba-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b69ba-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b69ba-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b69ba-131">INPUTS</span></span>

### <span data-ttu-id="b69ba-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b69ba-132">System.String</span></span>

### <span data-ttu-id="b69ba-133">System. Nullable ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b69ba-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="b69ba-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b69ba-134">OUTPUTS</span></span>

### <span data-ttu-id="b69ba-135">Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessSignatureAttributes</span><span class="sxs-lookup"><span data-stu-id="b69ba-135">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessSignatureAttributes</span></span>

## <span data-ttu-id="b69ba-136">Note</span><span class="sxs-lookup"><span data-stu-id="b69ba-136">NOTES</span></span>

## <span data-ttu-id="b69ba-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b69ba-137">RELATED LINKS</span></span>

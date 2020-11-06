---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAlert.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAlert.md
ms.openlocfilehash: 81cb94cdcb8efa948160d21da3aca709bb86b6fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513439"
---
# <span data-ttu-id="109a7-101">Set-AzureRmSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="109a7-101">Set-AzureRmSecurityAlert</span></span>

## <span data-ttu-id="109a7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="109a7-102">SYNOPSIS</span></span>
<span data-ttu-id="109a7-103">Aggiorna uno stato di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="109a7-103">Updates a security alert state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="109a7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="109a7-104">SYNTAX</span></span>

### <span data-ttu-id="109a7-105">SubscriptionLevelResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="109a7-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzureRmSecurityAlert -Location <String> -Name <String> -ActionType <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="109a7-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="109a7-106">ResourceGroupLevelResource</span></span>
```
Set-AzureRmSecurityAlert -ResourceGroupName <String> -Location <String> -Name <String> -ActionType <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="109a7-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="109a7-107">ResourceId</span></span>
```
Set-AzureRmSecurityAlert -ActionType <String> -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="109a7-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="109a7-108">InputObject</span></span>
```
Set-AzureRmSecurityAlert [-ActionType <String>] -InputObject <PSSetAlertInputObject> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="109a7-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="109a7-109">DESCRIPTION</span></span>
<span data-ttu-id="109a7-110">Imposta uno stato di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="109a7-110">Sets a security alert state.</span></span>

## <span data-ttu-id="109a7-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="109a7-111">EXAMPLES</span></span>

### <span data-ttu-id="109a7-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="109a7-112">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityAlert -Location "centralus" -ResourceGroupName "RSG" -Name "2518710774294070750_FFF23C70-80EF-4A8B-9122-507B0EA8DFFF" -ActionType Dismiss
```

<span data-ttu-id="109a7-113">Respinge un avviso di sicurezza generato.</span><span class="sxs-lookup"><span data-stu-id="109a7-113">Dismisses a security alert that was raised.</span></span>

## <span data-ttu-id="109a7-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="109a7-114">PARAMETERS</span></span>

### <span data-ttu-id="109a7-115">-ActionType</span><span class="sxs-lookup"><span data-stu-id="109a7-115">-ActionType</span></span>
<span data-ttu-id="109a7-116">Tipo di azione.</span><span class="sxs-lookup"><span data-stu-id="109a7-116">Action Type.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="109a7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="109a7-117">-DefaultProfile</span></span>
<span data-ttu-id="109a7-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="109a7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="109a7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="109a7-119">-InputObject</span></span>
<span data-ttu-id="109a7-120">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="109a7-120">Input Object.</span></span>

```yaml
Type: PSSetAlertInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="109a7-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="109a7-121">-Location</span></span>
<span data-ttu-id="109a7-122">Posizione.</span><span class="sxs-lookup"><span data-stu-id="109a7-122">Location.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="109a7-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="109a7-123">-Name</span></span>
<span data-ttu-id="109a7-124">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="109a7-124">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="109a7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="109a7-125">-PassThru</span></span>
<span data-ttu-id="109a7-126">Restituirà se l'operazione è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="109a7-126">Return whether the operation was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="109a7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="109a7-127">-ResourceGroupName</span></span>
<span data-ttu-id="109a7-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="109a7-128">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="109a7-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="109a7-129">-ResourceId</span></span>
<span data-ttu-id="109a7-130">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="109a7-130">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="109a7-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="109a7-131">-Confirm</span></span>
<span data-ttu-id="109a7-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="109a7-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="109a7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="109a7-133">-WhatIf</span></span>
<span data-ttu-id="109a7-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="109a7-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="109a7-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="109a7-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="109a7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="109a7-136">CommonParameters</span></span>
<span data-ttu-id="109a7-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="109a7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="109a7-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="109a7-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="109a7-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="109a7-139">INPUTS</span></span>

### <span data-ttu-id="109a7-140">System. String</span><span class="sxs-lookup"><span data-stu-id="109a7-140">System.String</span></span>
<span data-ttu-id="109a7-141">Microsoft. Azure. Commands. Security. Cmdlets. alerts. PSSetAlertInputObject</span><span class="sxs-lookup"><span data-stu-id="109a7-141">Microsoft.Azure.Commands.Security.Cmdlets.Alerts.PSSetAlertInputObject</span></span>

## <span data-ttu-id="109a7-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="109a7-142">OUTPUTS</span></span>

### <span data-ttu-id="109a7-143">Microsoft. Azure. Commands. Security. Models. alerts. PSSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="109a7-143">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span></span>

## <span data-ttu-id="109a7-144">Note</span><span class="sxs-lookup"><span data-stu-id="109a7-144">NOTES</span></span>

## <span data-ttu-id="109a7-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="109a7-145">RELATED LINKS</span></span>
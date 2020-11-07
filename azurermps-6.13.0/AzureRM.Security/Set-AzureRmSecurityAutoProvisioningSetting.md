---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAutoProvisioningSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAutoProvisioningSetting.md
ms.openlocfilehash: e99ead17cad0a3c6c440967ec1b1852bb5568a26
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686042"
---
# <span data-ttu-id="75232-101">Set-AzureRmSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="75232-101">Set-AzureRmSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="75232-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="75232-102">SYNOPSIS</span></span>
<span data-ttu-id="75232-103">Impostazione di provisioning automatico degli aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="75232-103">Updates automatic provisioning setting</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75232-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="75232-104">SYNTAX</span></span>

### <span data-ttu-id="75232-105">SubscriptionLevelResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="75232-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzureRmSecurityAutoProvisioningSetting -Name <String> [-EnableAutoProvision]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75232-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="75232-106">ResourceId</span></span>
```
Set-AzureRmSecurityAutoProvisioningSetting [-EnableAutoProvision] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75232-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="75232-107">InputObject</span></span>
```
Set-AzureRmSecurityAutoProvisioningSetting -InputObject <PSSecurityAutoProvisioningSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75232-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75232-108">DESCRIPTION</span></span>
<span data-ttu-id="75232-109">Attiva o disattiva le impostazioni di provisioning automatico per un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="75232-109">Turns on or off automatic provisioning settings for a subscription.</span></span>
<span data-ttu-id="75232-110">Le impostazioni di provisioning automatico consentono di decidere se si vuole che Azure Security Center provisiona automaticamente un agente di sicurezza che verrà installato nella propria VM.</span><span class="sxs-lookup"><span data-stu-id="75232-110">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="75232-111">L'agente di sicurezza controllerà la VM per creare avvisi di sicurezza e monitorare la conformità della sicurezza della VM.</span><span class="sxs-lookup"><span data-stu-id="75232-111">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="75232-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="75232-112">EXAMPLES</span></span>

### <span data-ttu-id="75232-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="75232-113">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityAutoProvisioningSetting -Name "default" -EnableAutoProvision
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="75232-114">Attiva l'impostazione di provisioning automatico per un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="75232-114">Turns on automatic provisioning setting for a subscription.</span></span>

### <span data-ttu-id="75232-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="75232-115">Example 2</span></span>
```powershell
PS C:\> Set-AzureRmSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name 
--                                                                                                                ---- 
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default de...
```

<span data-ttu-id="75232-116">Disattiva l'impostazione di provisioning automatico per un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="75232-116">Turns off automatic provisioning setting for a subscription.</span></span>

## <span data-ttu-id="75232-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="75232-117">PARAMETERS</span></span>

### <span data-ttu-id="75232-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75232-118">-DefaultProfile</span></span>
<span data-ttu-id="75232-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="75232-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75232-120">-EnableAutoProvision</span><span class="sxs-lookup"><span data-stu-id="75232-120">-EnableAutoProvision</span></span>
<span data-ttu-id="75232-121">Provisioning automatico.</span><span class="sxs-lookup"><span data-stu-id="75232-121">Automatic Provisioning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SubscriptionLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75232-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75232-122">-InputObject</span></span>
<span data-ttu-id="75232-123">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="75232-123">Input Object.</span></span>

```yaml
Type: PSSecurityAutoProvisioningSetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75232-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="75232-124">-Name</span></span>
<span data-ttu-id="75232-125">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="75232-125">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75232-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75232-126">-ResourceId</span></span>
<span data-ttu-id="75232-127">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="75232-127">Resource ID.</span></span>

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

### <span data-ttu-id="75232-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="75232-128">-Confirm</span></span>
<span data-ttu-id="75232-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75232-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75232-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75232-130">-WhatIf</span></span>
<span data-ttu-id="75232-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="75232-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75232-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="75232-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75232-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75232-133">CommonParameters</span></span>
<span data-ttu-id="75232-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75232-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75232-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75232-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75232-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="75232-136">INPUTS</span></span>

### <span data-ttu-id="75232-137">System. String</span><span class="sxs-lookup"><span data-stu-id="75232-137">System.String</span></span>
<span data-ttu-id="75232-138">System. Management. Automation. SwitchParameter Microsoft. Azure. Commands. Security. Models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="75232-138">System.Management.Automation.SwitchParameter Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="75232-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="75232-139">OUTPUTS</span></span>

### <span data-ttu-id="75232-140">Microsoft. Azure. Commands. Security. Models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="75232-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="75232-141">Note</span><span class="sxs-lookup"><span data-stu-id="75232-141">NOTES</span></span>

## <span data-ttu-id="75232-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="75232-142">RELATED LINKS</span></span>

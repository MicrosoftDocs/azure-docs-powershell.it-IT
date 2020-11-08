---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: f3d30608230fffc934a3cfcf9a4b15264dbcf008
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201462"
---
# <span data-ttu-id="63338-101">Set-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="63338-101">Set-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="63338-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="63338-102">SYNOPSIS</span></span>
<span data-ttu-id="63338-103">Impostazione di provisioning automatico degli aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="63338-103">Updates automatic provisioning setting</span></span>

## <span data-ttu-id="63338-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="63338-104">SYNTAX</span></span>

### <span data-ttu-id="63338-105">SubscriptionLevelResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="63338-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAutoProvisioningSetting -Name <String> [-EnableAutoProvision]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63338-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="63338-106">ResourceId</span></span>
```
Set-AzSecurityAutoProvisioningSetting [-EnableAutoProvision] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63338-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="63338-107">InputObject</span></span>
```
Set-AzSecurityAutoProvisioningSetting -InputObject <PSSecurityAutoProvisioningSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63338-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63338-108">DESCRIPTION</span></span>
<span data-ttu-id="63338-109">Attiva o disattiva le impostazioni di provisioning automatico per un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="63338-109">Turns on or off automatic provisioning settings for a subscription.</span></span>
<span data-ttu-id="63338-110">Le impostazioni di provisioning automatico consentono di decidere se si vuole che Azure Security Center provisiona automaticamente un agente di sicurezza che verrà installato nella propria VM.</span><span class="sxs-lookup"><span data-stu-id="63338-110">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="63338-111">L'agente di sicurezza controllerà la VM per creare avvisi di sicurezza e monitorare la conformità della sicurezza della VM.</span><span class="sxs-lookup"><span data-stu-id="63338-111">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="63338-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="63338-112">EXAMPLES</span></span>

### <span data-ttu-id="63338-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="63338-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default" -EnableAutoProvision
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="63338-114">Attiva l'impostazione di provisioning automatico per un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="63338-114">Turns on automatic provisioning setting for a subscription.</span></span>

### <span data-ttu-id="63338-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="63338-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name 
--                                                                                                                ---- 
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default de...
```

<span data-ttu-id="63338-116">Disattiva l'impostazione di provisioning automatico per un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="63338-116">Turns off automatic provisioning setting for a subscription.</span></span>

## <span data-ttu-id="63338-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="63338-117">PARAMETERS</span></span>

### <span data-ttu-id="63338-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63338-118">-DefaultProfile</span></span>
<span data-ttu-id="63338-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="63338-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63338-120">-EnableAutoProvision</span><span class="sxs-lookup"><span data-stu-id="63338-120">-EnableAutoProvision</span></span>
<span data-ttu-id="63338-121">Provisioning automatico.</span><span class="sxs-lookup"><span data-stu-id="63338-121">Automatic Provisioning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SubscriptionLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63338-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63338-122">-InputObject</span></span>
<span data-ttu-id="63338-123">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="63338-123">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63338-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="63338-124">-Name</span></span>
<span data-ttu-id="63338-125">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="63338-125">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63338-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63338-126">-ResourceId</span></span>
<span data-ttu-id="63338-127">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="63338-127">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63338-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="63338-128">-Confirm</span></span>
<span data-ttu-id="63338-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63338-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63338-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63338-130">-WhatIf</span></span>
<span data-ttu-id="63338-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="63338-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="63338-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="63338-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63338-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63338-133">CommonParameters</span></span>
<span data-ttu-id="63338-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63338-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63338-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63338-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63338-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="63338-136">INPUTS</span></span>

### <span data-ttu-id="63338-137">System. String</span><span class="sxs-lookup"><span data-stu-id="63338-137">System.String</span></span>

### <span data-ttu-id="63338-138">Microsoft. Azure. Commands. Security. Models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="63338-138">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="63338-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="63338-139">OUTPUTS</span></span>

### <span data-ttu-id="63338-140">Microsoft. Azure. Commands. Security. Models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="63338-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="63338-141">Note</span><span class="sxs-lookup"><span data-stu-id="63338-141">NOTES</span></span>

## <span data-ttu-id="63338-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="63338-142">RELATED LINKS</span></span>

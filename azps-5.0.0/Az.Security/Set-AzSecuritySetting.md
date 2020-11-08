---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
ms.openlocfilehash: 09273ee53eb3e4ced7249505e73f4f9f39db5291
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199652"
---
# <span data-ttu-id="c6474-101">Set-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="c6474-101">Set-AzSecuritySetting</span></span>

## <span data-ttu-id="c6474-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c6474-102">SYNOPSIS</span></span>
<span data-ttu-id="c6474-103">Aggiornare un'impostazione di sicurezza in Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="c6474-103">Update a security setting in Azure Security Center</span></span>

## <span data-ttu-id="c6474-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c6474-104">SYNTAX</span></span>

### <span data-ttu-id="c6474-105">GeneralScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c6474-105">GeneralScope (Default)</span></span>
```
Set-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6474-106">DataExportSettingsScope</span><span class="sxs-lookup"><span data-stu-id="c6474-106">DataExportSettingsScope</span></span>
```
Set-AzSecuritySetting -SettingName <String> -SettingKind <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6474-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="c6474-107">InputObject</span></span>
```
Set-AzSecuritySetting -InputObject <PSSecuritySetting> [-Enabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6474-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c6474-108">DESCRIPTION</span></span>
<span data-ttu-id="c6474-109">Il cmdlet Set-AzSecuritySetting aggiorna una specifica impostazione di sicurezza in Azure Security Center.</span><span class="sxs-lookup"><span data-stu-id="c6474-109">The Set-AzSecuritySetting cmdlet updates a specific security setting in Azure Security Center.</span></span>

## <span data-ttu-id="c6474-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c6474-110">EXAMPLES</span></span>

### <span data-ttu-id="c6474-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c6474-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS" -SettingKind "DataExportSettings" -Enabled $true

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="c6474-112">Aggiorna un'impostazione di esportazione dei dati di MCAS</span><span class="sxs-lookup"><span data-stu-id="c6474-112">Updates an MCAS data export setting</span></span>   

## <span data-ttu-id="c6474-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c6474-113">PARAMETERS</span></span>

### <span data-ttu-id="c6474-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6474-114">-DefaultProfile</span></span>
<span data-ttu-id="c6474-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c6474-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6474-116">-Enabled</span><span class="sxs-lookup"><span data-stu-id="c6474-116">-Enabled</span></span>
<span data-ttu-id="c6474-117">Abilita l'impostazione.</span><span class="sxs-lookup"><span data-stu-id="c6474-117">Enables the setting.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: DataExportSettingsScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Boolean
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6474-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6474-118">-InputObject</span></span>
<span data-ttu-id="c6474-119">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="c6474-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6474-120">-SettingKind</span><span class="sxs-lookup"><span data-stu-id="c6474-120">-SettingKind</span></span>
<span data-ttu-id="c6474-121">Tipo di impostazione.</span><span class="sxs-lookup"><span data-stu-id="c6474-121">Setting kind.</span></span> <span data-ttu-id="c6474-122">(DataExportSettings)</span><span class="sxs-lookup"><span data-stu-id="c6474-122">(DataExportSettings)</span></span>

```yaml
Type: System.String
Parameter Sets: DataExportSettingsScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6474-123">-SettingName</span><span class="sxs-lookup"><span data-stu-id="c6474-123">-SettingName</span></span>
<span data-ttu-id="c6474-124">Impostazione del nome.</span><span class="sxs-lookup"><span data-stu-id="c6474-124">Setting name.</span></span> <span data-ttu-id="c6474-125">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="c6474-125">(MCAS/WDATP)</span></span>

```yaml
Type: System.String
Parameter Sets: DataExportSettingsScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6474-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c6474-126">-Confirm</span></span>
<span data-ttu-id="c6474-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6474-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6474-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6474-128">-WhatIf</span></span>
<span data-ttu-id="c6474-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c6474-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6474-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c6474-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6474-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6474-131">CommonParameters</span></span>
<span data-ttu-id="c6474-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6474-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6474-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6474-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6474-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c6474-134">INPUTS</span></span>

### <span data-ttu-id="c6474-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c6474-135">System.String</span></span>
### <span data-ttu-id="c6474-136">Microsoft. Azure. Commands. Security. Models. Settings. PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="c6474-136">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="c6474-137">Microsoft. Azure. Commands. Security. Models. Settings. PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="c6474-137">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

### <span data-ttu-id="c6474-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c6474-138">System.Boolean</span></span>

## <span data-ttu-id="c6474-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c6474-139">OUTPUTS</span></span>

### <span data-ttu-id="c6474-140">Microsoft. Azure. Commands. Security. Models. Settings. PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="c6474-140">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="c6474-141">Microsoft. Azure. Commands. Security. Models. Settings. PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="c6474-141">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="c6474-142">Note</span><span class="sxs-lookup"><span data-stu-id="c6474-142">NOTES</span></span>

## <span data-ttu-id="c6474-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c6474-143">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 3b433860cda56f827bb58bc135240da41b89ef93
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201783"
---
# <span data-ttu-id="c37a5-101">Set-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c37a5-101">Set-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="c37a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c37a5-102">SYNOPSIS</span></span>
<span data-ttu-id="c37a5-103">Imposta il criterio di protezione SQL tenant effettivo.</span><span class="sxs-lookup"><span data-stu-id="c37a5-103">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="c37a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c37a5-104">SYNTAX</span></span>

### <span data-ttu-id="c37a5-105">SQL di protezione delle informazioni personali (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c37a5-105">SQL Information Protection Policy (Default)</span></span>
```
Set-AzSqlInformationProtectionPolicy -Policy <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c37a5-106">SQL del file dei criteri di protezione delle informazioni</span><span class="sxs-lookup"><span data-stu-id="c37a5-106">SQL Information Protection Policy File Path</span></span>
```
Set-AzSqlInformationProtectionPolicy -FilePath <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c37a5-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c37a5-107">DESCRIPTION</span></span>
<span data-ttu-id="c37a5-108">Imposta il criterio di protezione SQL tenant effettivo.</span><span class="sxs-lookup"><span data-stu-id="c37a5-108">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="c37a5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c37a5-109">EXAMPLES</span></span>

### <span data-ttu-id="c37a5-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="c37a5-110">Example</span></span>
```powershell
PS C:\> Set-AzSqlInformationProtectionPolicy -FilePath "C:\Users\myUser\Desktop\policy.json"
```

## <span data-ttu-id="c37a5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c37a5-111">PARAMETERS</span></span>

### <span data-ttu-id="c37a5-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c37a5-112">-AsJob</span></span>
<span data-ttu-id="c37a5-113">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c37a5-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c37a5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c37a5-114">-DefaultProfile</span></span>
<span data-ttu-id="c37a5-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c37a5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c37a5-116">-FilePath</span><span class="sxs-lookup"><span data-stu-id="c37a5-116">-FilePath</span></span>
<span data-ttu-id="c37a5-117">Specifica il percorso di un file JSON contenente SQL definizione dei criteri di protezione delle informazioni.</span><span class="sxs-lookup"><span data-stu-id="c37a5-117">Specifies a path of a .json file containing SQL Information Protection Policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: SQL Information Protection Policy File Path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c37a5-118">-Policy</span><span class="sxs-lookup"><span data-stu-id="c37a5-118">-Policy</span></span>
<span data-ttu-id="c37a5-119">Specifica una definizione SQL dei criteri di protezione delle informazioni personali.</span><span class="sxs-lookup"><span data-stu-id="c37a5-119">Specifies a SQL information protection policy definition.</span></span> <span data-ttu-id="c37a5-120">È possibile specificare il percorso di un file JSON o di una stringa in formato JSON che definisce il criterio.</span><span class="sxs-lookup"><span data-stu-id="c37a5-120">You can specify a path of a .json file or a JSON format string that defines the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SQL Information Protection Policy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c37a5-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c37a5-121">-Confirm</span></span>
<span data-ttu-id="c37a5-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c37a5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c37a5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c37a5-123">-WhatIf</span></span>
<span data-ttu-id="c37a5-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c37a5-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c37a5-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c37a5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c37a5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c37a5-126">CommonParameters</span></span>
<span data-ttu-id="c37a5-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c37a5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c37a5-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c37a5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c37a5-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="c37a5-129">INPUTS</span></span>

### <span data-ttu-id="c37a5-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c37a5-130">System.String</span></span>

## <span data-ttu-id="c37a5-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c37a5-131">OUTPUTS</span></span>

### <span data-ttu-id="c37a5-132">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c37a5-132">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="c37a5-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="c37a5-133">NOTES</span></span>

## <span data-ttu-id="c37a5-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c37a5-134">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 3b433860cda56f827bb58bc135240da41b89ef93
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486248"
---
# <span data-ttu-id="bac56-101">Set-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="bac56-101">Set-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="bac56-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bac56-102">SYNOPSIS</span></span>
<span data-ttu-id="bac56-103">Imposta i criteri di protezione delle informazioni SQL del tenant effettivo.</span><span class="sxs-lookup"><span data-stu-id="bac56-103">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="bac56-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bac56-104">SYNTAX</span></span>

### <span data-ttu-id="bac56-105">Criteri di protezione delle informazioni SQL (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bac56-105">SQL Information Protection Policy (Default)</span></span>
```
Set-AzSqlInformationProtectionPolicy -Policy <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bac56-106">Percorso file di criteri di protezione delle informazioni SQL</span><span class="sxs-lookup"><span data-stu-id="bac56-106">SQL Information Protection Policy File Path</span></span>
```
Set-AzSqlInformationProtectionPolicy -FilePath <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bac56-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bac56-107">DESCRIPTION</span></span>
<span data-ttu-id="bac56-108">Imposta i criteri di protezione delle informazioni SQL del tenant effettivo.</span><span class="sxs-lookup"><span data-stu-id="bac56-108">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="bac56-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bac56-109">EXAMPLES</span></span>

### <span data-ttu-id="bac56-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="bac56-110">Example</span></span>
```powershell
PS C:\> Set-AzSqlInformationProtectionPolicy -FilePath "C:\Users\myUser\Desktop\policy.json"
```

## <span data-ttu-id="bac56-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bac56-111">PARAMETERS</span></span>

### <span data-ttu-id="bac56-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bac56-112">-AsJob</span></span>
<span data-ttu-id="bac56-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="bac56-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bac56-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bac56-114">-DefaultProfile</span></span>
<span data-ttu-id="bac56-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bac56-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bac56-116">-FilePath</span><span class="sxs-lookup"><span data-stu-id="bac56-116">-FilePath</span></span>
<span data-ttu-id="bac56-117">Specifica un percorso di un file con estensione JSON che contiene la definizione dei criteri di protezione delle informazioni SQL.</span><span class="sxs-lookup"><span data-stu-id="bac56-117">Specifies a path of a .json file containing SQL Information Protection Policy definition.</span></span>

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

### <span data-ttu-id="bac56-118">-Policy</span><span class="sxs-lookup"><span data-stu-id="bac56-118">-Policy</span></span>
<span data-ttu-id="bac56-119">Specifica una definizione di criteri di protezione delle informazioni SQL.</span><span class="sxs-lookup"><span data-stu-id="bac56-119">Specifies a SQL information protection policy definition.</span></span> <span data-ttu-id="bac56-120">Puoi specificare un percorso di un file con estensione JSON o una stringa di formato JSON che definisce i criteri.</span><span class="sxs-lookup"><span data-stu-id="bac56-120">You can specify a path of a .json file or a JSON format string that defines the policy.</span></span>

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

### <span data-ttu-id="bac56-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bac56-121">-Confirm</span></span>
<span data-ttu-id="bac56-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bac56-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bac56-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bac56-123">-WhatIf</span></span>
<span data-ttu-id="bac56-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bac56-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bac56-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bac56-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bac56-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bac56-126">CommonParameters</span></span>
<span data-ttu-id="bac56-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bac56-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bac56-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bac56-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bac56-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bac56-129">INPUTS</span></span>

### <span data-ttu-id="bac56-130">System. String</span><span class="sxs-lookup"><span data-stu-id="bac56-130">System.String</span></span>

## <span data-ttu-id="bac56-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bac56-131">OUTPUTS</span></span>

### <span data-ttu-id="bac56-132">Microsoft. Azure. Commands. SecurityCenter. Models. SqlInformationProtectionPolicy. PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="bac56-132">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="bac56-133">Note</span><span class="sxs-lookup"><span data-stu-id="bac56-133">NOTES</span></span>

## <span data-ttu-id="bac56-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bac56-134">RELATED LINKS</span></span>

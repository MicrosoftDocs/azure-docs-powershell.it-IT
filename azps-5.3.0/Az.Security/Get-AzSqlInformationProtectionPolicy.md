---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 7f84c3b10577eea0d035c2ce84b3aa8a61af4a3d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486311"
---
# <span data-ttu-id="45133-101">Get-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="45133-101">Get-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="45133-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="45133-102">SYNOPSIS</span></span>
<span data-ttu-id="45133-103">Recupera i criteri di protezione delle informazioni SQL del tenant effettivo.</span><span class="sxs-lookup"><span data-stu-id="45133-103">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="45133-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="45133-104">SYNTAX</span></span>

```
Get-AzSqlInformationProtectionPolicy [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45133-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45133-105">DESCRIPTION</span></span>
<span data-ttu-id="45133-106">Recupera i criteri di protezione delle informazioni SQL del tenant effettivo.</span><span class="sxs-lookup"><span data-stu-id="45133-106">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="45133-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="45133-107">EXAMPLES</span></span>

### <span data-ttu-id="45133-108">Esempio</span><span class="sxs-lookup"><span data-stu-id="45133-108">Example</span></span>
```powershell
PS C:\> Get-AzSqlInformationProtectionPolicy
```

## <span data-ttu-id="45133-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="45133-109">PARAMETERS</span></span>

### <span data-ttu-id="45133-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45133-110">-AsJob</span></span>
<span data-ttu-id="45133-111">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="45133-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="45133-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45133-112">-DefaultProfile</span></span>
<span data-ttu-id="45133-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="45133-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45133-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45133-114">CommonParameters</span></span>
<span data-ttu-id="45133-115">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45133-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45133-116">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45133-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45133-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="45133-117">INPUTS</span></span>

### <span data-ttu-id="45133-118">System. String</span><span class="sxs-lookup"><span data-stu-id="45133-118">System.string</span></span>

## <span data-ttu-id="45133-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="45133-119">OUTPUTS</span></span>

### <span data-ttu-id="45133-120">Microsoft. Azure. Commands. SecurityCenter. Models. SqlInformationProtectionPolicy. PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="45133-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="45133-121">Note</span><span class="sxs-lookup"><span data-stu-id="45133-121">NOTES</span></span>

## <span data-ttu-id="45133-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="45133-122">RELATED LINKS</span></span>

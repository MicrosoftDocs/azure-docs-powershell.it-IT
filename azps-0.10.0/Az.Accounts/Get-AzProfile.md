---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzProfile.md
ms.openlocfilehash: d541c943c8dc9779cdf340440078ca2fd2fb36e1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860209"
---
# <span data-ttu-id="f17db-101">Get-AzProfile</span><span class="sxs-lookup"><span data-stu-id="f17db-101">Get-AzProfile</span></span>

## <span data-ttu-id="f17db-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f17db-102">SYNOPSIS</span></span>
<span data-ttu-id="f17db-103">Ottenere i profili di servizio supportati da moduli installati.</span><span class="sxs-lookup"><span data-stu-id="f17db-103">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="f17db-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f17db-104">SYNTAX</span></span>

```
Get-AzProfile [-ModuleName <String[]>] [-ListAvailable] [<CommonParameters>]
```

## <span data-ttu-id="f17db-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f17db-105">DESCRIPTION</span></span>
<span data-ttu-id="f17db-106">Ottenere i profili di servizio supportati da moduli installati.</span><span class="sxs-lookup"><span data-stu-id="f17db-106">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="f17db-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f17db-107">EXAMPLES</span></span>

### <span data-ttu-id="f17db-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f17db-108">Example 1</span></span>
```powershell
PS C:\> Get-AzProfile -ModuleName Az.KeyVault

Name              Description
----              -----------
latest-2019-04-30 A snapshot of the service API versions in the Azure Global Cloud. This profile was defined in April 2019.
hybrid-2019-03-01 A snapshot of the Service API versions in AzureStack, Azure Sovereign clouds, and the Azure Global Cloud. This profile was defined                    in March 2019.
```

<span data-ttu-id="f17db-109">Ottenere il profilo del servizio supportato dal modulo di Vault</span><span class="sxs-lookup"><span data-stu-id="f17db-109">Get the service profile supported by the KeyVault module</span></span>

## <span data-ttu-id="f17db-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f17db-110">PARAMETERS</span></span>

### <span data-ttu-id="f17db-111">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="f17db-111">-ListAvailable</span></span>
<span data-ttu-id="f17db-112">Elenca tutti i profili dei servizi supportati dai moduli installati</span><span class="sxs-lookup"><span data-stu-id="f17db-112">List all service profiles supported by installed modules</span></span>

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

### <span data-ttu-id="f17db-113">-ModuleName</span><span class="sxs-lookup"><span data-stu-id="f17db-113">-ModuleName</span></span>
<span data-ttu-id="f17db-114">Il nome del modulo da controllare</span><span class="sxs-lookup"><span data-stu-id="f17db-114">The name of the module to check</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f17db-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f17db-115">CommonParameters</span></span>
<span data-ttu-id="f17db-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f17db-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f17db-117">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f17db-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f17db-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f17db-118">INPUTS</span></span>

### <span data-ttu-id="f17db-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f17db-119">None</span></span>

## <span data-ttu-id="f17db-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f17db-120">OUTPUTS</span></span>

### <span data-ttu-id="f17db-121">Microsoft. Azure. Commands. profile. CommonModule. PSAzureServiceProfile</span><span class="sxs-lookup"><span data-stu-id="f17db-121">Microsoft.Azure.Commands.Profile.CommonModule.PSAzureServiceProfile</span></span>

## <span data-ttu-id="f17db-122">Note</span><span class="sxs-lookup"><span data-stu-id="f17db-122">NOTES</span></span>

## <span data-ttu-id="f17db-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f17db-123">RELATED LINKS</span></span>
